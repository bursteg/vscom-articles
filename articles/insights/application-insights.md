<properties
	pageTitle="What is Application Insights?"
  description="What is Application Insights?"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 

# What is Application Insights?


*Application Insights is in Preview.*



[Visual Studio Application Insights](https://azure.microsoft.com/services/application-insights) is an extensible analytics service that helps you understand the performance and usage of your live application. It's designed for developers, to help you continuously improve the performance and usability of your app.



It works with both web and stand-alone apps on a wide variety of platforms: .NET or J2EE, hosted on-premises or in the cloud; device apps on Windows, iOS, Android, OSX and other platforms.



It is aimed at the development team. With it, you can:


- [Analyze usage patterns](https://azure.microsoft.com/documentation/articles/app-insights-overview-usage/) to understand your users better and continuously improve your app. 
 - Page view counts, new and returning users, geolocation, platforms, and other core usage statistics
 - Trace usage paths to assess the success of each feature.
- [Detect, triage and diagnose](https://azure.microsoft.com/documentation/articles/app-insights-detect-triage-diagnose/) performance issues and fix them before most of your users are aware.
 - Alerts on performance changes or crashes.
 - Metrics to help diagnose performance issues, such as response times, CPU usage, dependency tracking.
 - Availability tests for web apps.
 - Crash and exception reports and alerts
 - Powerful diagnostic log search (including log traces from your favorite logging frameworks).


The SDK for each platform includes a range of modules that monitor the app straight out of the box. In addition, you can code your own telemetry for more detailed and tailored analytics.



Telemetry data collected from your application is stored and analysed in the Azure Portal, where there are intuitive views and powerful tools for fast diagnosis and analysis.



![Chart user activity statistics, or drill into specific events.](./media/application-insights/00-sample.png)


## Platforms and languages


There are SDKs for a growing range of platforms. Currently the list includes:


- [ASP.NET servers](https://azure.microsoft.com/documentation/articles/app-insights-start-monitoring-app-health-usage/) on Azure or your IIS server
- [Azure Cloud Services](https://azure.microsoft.com/documentation/articles/app-insights-cloudservices/)
- [J2EE servers](https://azure.microsoft.com/documentation/articles/app-insights-java-get-started/)
- [Web pages](https://azure.microsoft.com/documentation/articles/app-insights-javascript/): HTML+JavaScript
- [Windows Phone, Windows Store, Windows 10 universal apps, and direct integration with the Windows 10 developer portal](https://azure.microsoft.com/documentation/articles/app-insights-windows-get-started/)
- [Windows desktop](https://azure.microsoft.com/documentation/articles/app-insights-windows-desktop/)
- [iOS](https://azure.microsoft.com/documentation/articles/app-insights-ios/)
- [Android](https://azure.microsoft.com/documentation/articles/app-insights-android/)
- [Other platforms](https://azure.microsoft.com/documentation/articles/app-insights-platforms/) - Node.js, PHP, Python, Ruby, Joomla, SharePoint, WordPress


Application Insights can also get telemetry from existing ASP.NET web apps on IIS without rebuilding them.



If your app has client, server and other components, you can instrument them all. The data will be integrated in the Application Insights portal so that, for example, you can correlate events at the client with events at the server.


## How it works


You install a small SDK in your application, and set up an account in the Application Insights portal. The SDK monitors your app and sends telemetry data to the portal. The portal shows you statistical charts and provides powerful search tools to help you diagnose any problems.



![The Application Insights SDK in your app sends telemetry to your Application Insights resource in the Azure portal.](./media/application-insights/01-scheme.png)



The SDK has several modules which collect telemetry, for example to count users, sessions, and performance. You can also write your own custom code to send telemetry data to the portal. Custom telemetry is particularly useful to trace user stories: you can count events such as button clicks, achievement of particular goals, or user mistakes.



For ASP.NET servers and Azure web apps, you can also install [Status Monitor](https://azure.microsoft.com/documentation/articles/app-insights-monitor-performance-live-website-now/), which has two uses. It lets you:


- Monitor a web app without re-building or re-installing it.
- Track calls to dependent modules.

### What's the overhead?


The impact on your performance is very small. Tracking calls non-blocking, and are batched and sent in a separate thread.


## To get started

1. You'll need a subscription to [Microsoft Azure](https://azure.com). It's free to sign up, and you can choose the free [pricing tier](https://azure.microsoft.com/pricing/details/application-insights/) of Application Insights.
2. Sign into [Azure Preview Portal](https://portal.azure.com)
3. Create an Application Insights resource. This is where you'll see data from your app.



![Add, Developer Services, Application Insights.](./media/application-insights/11-new.png)



Choose your application type.
4. Open your new resource, and open the Quick Start guide.



![Browse, ](./media/application-insights/quickstart.png)



This explains how to install the SDK in your app. If it's a web app, you'll also find out how to add the SDK to web pages, and to set up availability tests.


For more details, choose your app type from [this list of platforms and languages](https://azure.microsoft.com/documentation/articles/app-insights-platforms/).


## Support and feedback

- Questions and Issues:
 - [Troubleshooting](https://azure.microsoft.com/documentation/articles/app-insights-troubleshoot-faq/)
 - [MSDN Forum](https://social.msdn.microsoft.com/Forums/vstudio/en-US/home?forum=ApplicationInsights)
 - [StackOverflow](http://stackoverflow.com/questions/tagged/ms-application-insights)
- Bugs:
 - [Connect](https://connect.microsoft.com/VisualStudio/Feedback/LoadSubmitFeedbackForm?FormID=6076)
- Suggestions:
 - [User Voice](http://visualstudio.uservoice.com/forums/121579-visual-studio/category/77108-application-insights)
