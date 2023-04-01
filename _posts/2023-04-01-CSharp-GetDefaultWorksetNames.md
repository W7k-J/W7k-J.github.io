---
layout: post  
title: C# - GetDefaultWorksetNames Method
date: 2023-04-01 12:00:00
author: Julian
---
![PostPage](/images/2023 CSharpGetDefaultWorksetNames/CSharpGetDefaultWorksetNames.png)

<!--excerpt-->


My code end up in the github of Jeremy Tammik, The building coder!  

[Link](https://github.com/jeremytammik/the_building_coder_samples/blob/master/BuildingCoder/Util.cs#L2144-L2238)
  
# Method GetDefaultWorksetNames  

It is a default language checker which comes back with names for both default worksets. 

```csharp 
// Shared by Julian Wandzilak in the Revit API discussion thread
// https://forums.autodesk.com/t5/revit-api-forum/doc-enableworksharing-amp-language-versions/m-p/11845252#M70159
/// <summary>
/// Return default workset names 
/// for all languages supported by Revit
/// </summary>
/// <param name="sLanguage">`app.Language.ToString()`</param>
/// <returns>`false` if no valid language input argument provided, else `true`</returns>
bool GetDefaultWorksetNames(
    string sLanguage,
    out string wsnLevelsAndGrids,
    out string wsnWorkset1)
{
    wsnLevelsAndGrids = string.Empty;
    wsnWorkset1 = string.Empty;

    switch (sLanguage)
    {
        case "Unknown":
            wsnLevelsAndGrids = "Shared Levels and Grids";
            wsnWorkset1 = "Workset1";
            break;
        case "English_USA":
            wsnLevelsAndGrids = "Shared Levels and Grids";
            wsnWorkset1 = "Workset1";
            break;
        case "German":
            wsnLevelsAndGrids = "Gemeinsam genutzte Ebenen und Raster";
            wsnWorkset1 = "Bearbeitungsbereich1";
            break;
        case "Spanish":
            wsnLevelsAndGrids = "Niveles y rejillas compartidos";
            wsnWorkset1 = "Subproyecto1";
            break;
        case "French":
            wsnLevelsAndGrids = "Quadrillages et niveaux partagés";
            wsnWorkset1 = "Sous-projet 1";
            break;
        case "Italian":
            wsnLevelsAndGrids = "Griglie e livelli condivisi";
            wsnWorkset1 = "Workset1";
            break;
        //case "Dutch":
        //  wsnLevelsAndGrids = "Shared Levels and Grids";
        //  wsnWorkset1 = "Workset1";
        //  break;
        case "Chinese_Simplified":
            wsnLevelsAndGrids = "共享标高和轴网";
            wsnWorkset1 = "工作集1";
            break;
        case "Chinese_Traditional":
            wsnLevelsAndGrids = "共用的樓層和網格";
            wsnWorkset1 = "工作集 1";
            break;
        case "Japanese":
            wsnLevelsAndGrids = "共有レベルと通芯";
            wsnWorkset1 = "ワークセット1";
            break;
        case "Korean":
            wsnLevelsAndGrids = "공유 레벨 및 그리드";
            wsnWorkset1 = "작업세트1";
            break;
        case "Russian":
            wsnLevelsAndGrids = "Общие уровни и сетки";
            wsnWorkset1 = "Рабочий набор 1";
            break;
        case "Czech":
            wsnLevelsAndGrids = "Sdílená podlaží a osnovy";
            wsnWorkset1 = "Pracovní sada1";
            break;
        case "Polish":
            wsnLevelsAndGrids = "Współdzielone poziomy i osie";
            wsnWorkset1 = "Zadanie1";
            break;
        //case "Hungarian":
        //  wsnLevelsAndGrids = "Shared Levels and Grids";
        //  wsnWorkset1 = "Workset1";
        //  break;
        case "Brazilian_Portuguese":
            wsnLevelsAndGrids = "Níveis e eixos compartilhados";
            wsnWorkset1 = "Workset1";
            break;
        case "English_GB":
            wsnLevelsAndGrids = "Shared Levels and Grids";
            wsnWorkset1 = "Workset1";
            break;
        default:
            wsnLevelsAndGrids = "Shared Levels and Grids";
            wsnWorkset1 = "Workset1";
            break;
    }
    return 0 < wsnLevelsAndGrids.Length;
}
```
  
  There is an "Unknown type" - I didn't know if I should add it (default in a switch would cover it). In the end, I left it in the code. What should we do to get this type from revit api? 

 

There are some interesting findings in it. Firstly, we have two langagueType (hungarian and dutch) in Revit API. I couldn't find them in language help.
https://help.autodesk.com/view/RVT/2023/ENU/?guid=GUID-BD09C1B4-5520-475D-BE7E-773642EEBD6C

I assumed that those language versions are being developed, so for now I commented them out in the code.

 

Also, it is interesting that some translators decided to keep Workset1 as default - We have it not only in English but also in Italian and Brazilian Portuguese. I like this approach because in my opinion, Polish translation "Zadanie1" is rather bad and confusing (it means something closer to "task"). Because of that I saw some projects where worksets were named "Tasks of Adam", "Tasks of Kate" etc.

 

The other interesting thing is lack of consistency regarding number "1". In most languages we don't have extra space between Workset and 1, but in Russian, French and traditional Chinese with have. Chinese is double interesting because in simplified Chinese we don't have empty space.