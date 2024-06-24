---
layout: post  
title: Entitlement Revit API - My update

date: 2024-05-08 12:00:00
author: Julian
---
![PostPage](/images/2024_BlogPost/CheckOnline.jpg)

<!--excerpt-->

I am recently updating all my paid apps to 2025 - Thanks to this forum, everything goes rather smooth. Except I had some weird problems with my CheckOnline method which was based on provided method here: https://adndevblog.typepad.com/aec/2015/04/entitlement-api-for-revit-exchange-store-apps.html
  
For some reason in 2025 I had some problems with RestSharp -> while checking the license during OnApplicationInitialized method, the process was abruptly stopped, weirdly enough, without even throwing errors on me.
  

Update helped but as RestSharp change I started having problems with older revit versions. I decided to rewrite it completely, but this time using default HttpClient:  

>This method ended up on BuildingCoder blog. You will also find some other views there I shared on RevitAPI forum  
>
>[Link](https://thebuildingcoder.typepad.com/blog/2024/06/entitlement-api-for-revit-licensing-for-add-ins.html)

```c#

public static bool CheckOnline(string appId, string userId)
{
    Uri uri = new Uri($"https://apps.exchange.autodesk.com/webservices/checkentitlement/?userid={userId}&appid={appId}");
    bool isValid = false;

    try
    {
        HttpClient myHttpClient = new HttpClient();

        Task<HttpResponseMessage> task = Task.Run(() => myHttpClient.GetAsync(uri));
        task.Wait();
        HttpResponseMessage response = task.Result;

        Task<string> readTask = response.Content.ReadAsStringAsync();
        string text = readTask.Result;

        EntitlementResponse entitlementResponse = JsonConvert.DeserializeObject<EntitlementResponse>(text);

        isValid = entitlementResponse.IsValid;
    }
    catch
    {
        return false;
    }

    return isValid;
}

[Serializable]
public class EntitlementResponse
{
    public string UserId { get; set; }
    public string AppId { get; set; }
    public bool IsValid { get; set; }
    public string Message { get; set; }
}

```


