---
layout: post  
title: What do you do when you need to export multiple schedules as CSV from Revit?
date: 2025-11-17 12:00:00
author: Julian
thumbnail: /images/thumbs/2025_BlogPost/Academy3_Export.jpg
---
![PostPage](/images/2025_BlogPost/Academy3_Export.jpg)

<!--excerpt-->


# What do you do when you need to export multiple schedules as CSV from Revit?

Today, we faced the task of exporting more than **30 Revit schedules** to CSV.

By default, **Revit 2023 only allows you to export schedules one by one**, and there’s no built-in option to export several at once. Since we know this will become a recurring task, I volunteered to handle it myself.

And of course, I didn’t do it manually 😉. Instead, I wrote a **short macro**. Over the past months, my programming skills have improved to the point where I can confidently rely on AI for assistance—I’m much better at spotting mistakes in code, and my understanding of the code is also much deeper.

I let AI generate the initial code. It made **five small mistakes**, which I quickly corrected. Overall, the code was a good starting point: it didn’t work out of the box, but it looked solid and gave me a clear direction.

---

## What the macro does (brief explanation)

Below the short explanation and the code ready to be used

1. **Standard boilerplate** for `Document` and `UIDocument` – your starting point for any Revit macro.
2. **Getting user selection** and checking against an empty ID. It’s not perfect, but this is a Revit macro where I assume users know what they’re doing… At least they need to be able to select some schedules before running it.
3. **Defining the path** for exported schedules (I used the desktop). Feel free to change it. Personally, I treat my desktop as a workspace, so I’m fine with files landing there.
4. **Simple loop** through the selection.
5. **Check if the ID references a schedule.**
6. **Revit API class for export settings.** If you’re curious, read more about CSV and Revit schedule export options.
7. **Delimiter choice:** I used `^` after giving it some thought—it’s a character I don’t expect to see in my schedules. Swap it to a comma if you don’t expect commas in your schedules.
8. **ExportTextQualifier Enumeration:** Google this if you want to understand what’s happening here.
9. **Done.**

---

## Example Macro Code

```csharp
  
public void ExportSchedulesToCSV()
{
    UIDocument uidoc = this.ActiveUIDocument;
    Document doc = uidoc.Document;

    ICollection<ElementId> selectedIds = uidoc.Selection.GetElementIds();
    if (selectedIds.Count == 0)
    {
        TaskDialog.Show("Error", "Please select at least one schedule view.");
        return;
    }

    string desktopPath = Environment.GetFolderPath(Environment.SpecialFolder.Desktop);

    foreach (ElementId id in selectedIds)
    {
        ViewSchedule schedule = doc.GetElement(id) as ViewSchedule;
        if (schedule == null) continue;

        string fileName = Path.Combine(desktopPath, schedule.Name + ".csv");

        ViewScheduleExportOptions options = new ViewScheduleExportOptions();
        options.FieldDelimiter = "^"; // Change to comma if needed
        options.TextQualifier = ExportTextQualifier.DoubleQuote;

        schedule.Export(desktopPath, schedule.Name + ".csv", options);
    }

    TaskDialog.Show("Export Complete", "Schedules exported to Desktop.");
}
```  
