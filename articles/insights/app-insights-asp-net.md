
# Application Insights for ASP.NET


*Application Insights is in Preview.*



[Visual Studio Application Insights](https://azure.microsoft.com/services/application-insights) monitors your live application to help you [detect and diagnose performance issues and exceptions](https://azure.microsoft.com/documentation/articles/app-insights-detect-triage-diagnose/), and [discover how your app is used](https://azure.microsoft.com/documentation/articles/app-insights-overview-usage/). It can be used with a wide variety of application types. It works for apps that are hosted on your own on-premises IIS servers or on Azure VMs, as well as Azure web apps. ([Device apps and Java servers are also covered](https://azure.microsoft.com/documentation/articles/app-insights-get-started/).)



![Example performance monitoring charts](./media/app-insights-asp-net/10-perf.png)


#### Before you start


You need:


- A subscription to [Microsoft Azure](https://azure.com). If your team or organization has an Azure subscription, the owner can add you to it, using your [Microsoft account](https://live.com).
- Visual Studio 2013 update 3 or later.

## Add Application Insights to your project in Visual Studio

#### If it's a new project...


When you create a new project in Visual Studio, make sure Application Insights is selected.



![Create an ASP.NET project](./media/app-insights-asp-net/appinsights-01-vsnewp1.png)


#### ... or if it's an existing project


Right click the project in Solution Explorer, and choose Add Application Insights.



![Choose Add Application Insights](./media/app-insights-asp-net/appinsights-03-addExisting.png)


#### Setup options


If this is your first time, you'll be asked sign in or sign up to Microsoft Azure Preview. (It's separate from your Visual Studio Online account.)



If this app is part of a bigger application, you might want to use **Configure settings** to put it in the same resource group as the other components.


#### What did 'Add Application Insights' do?


The command did these steps (which you could instead do manually if you prefer):


- Creates an Application Insights resource in [the Azure portal](https://portal.azure.com/). This is where you'll see your data. It retrieves the *instrumentation key,* which identifies the resource.
- Adds the Application Insights Web SDK NuGet package to your project. To see it in Visual Studio, right-click your project and choose Manage NuGet Packages.
- Places the instrumentation key in `ApplicationInsights.config`.

## Run your project


Run your application with F5 and try it out: open different pages to generate some telemetry.



In Visual Studio, you'll see a count of the events that have been sent.



![On the debug toolbar, the Application Insights button shows a count of data points sent.](./media/app-insights-asp-net/appinsights-09eventcount.png)


## Open Application Insights


Open your Application Insights resource in the [Azure portal](https://portal.azure.com/).



![Right-click your project and open the Azure portal](./media/app-insights-asp-net/appinsights-04-openPortal.png)



Look for data in the Overview charts. At first, you'll just see one or two points. For example:



![Click through to more data](./media/app-insights-asp-net/12-first-perf.png)



Click through any chart to see more detailed metrics. [Learn more about metrics.](https://azure.microsoft.com/documentation/articles/app-insights-web-monitor-performance/)



Now deploy your application and watch the data accumulate.



When you run in debug mode, telemetry is expedited through the pipeline, so that you should see data appearing within seconds. When you deploy your app, data accumulates more slowly.


#### No data?

- Open the [Search](https://azure.microsoft.com/documentation/articles/app-insights-diagnostic-search/) tile, to see individual events.
- Use the application, opening different pages so that it generates some telemetry.
- Wait a few seconds and click Refresh.
- See [Troubleshooting](https://azure.microsoft.com/documentation/articles/app-insights-troubleshoot-faq/).

#### Trouble on your build server?


Please see [this Troubleshooting item](https://azure.microsoft.com/documentation/articles/app-insights-troubleshoot-faq.md#NuGetBuild).


## Add browser monitoring


Browser or client-side monitoring gives you data on users, sessions, page views, and any exceptions or crashes that occur in the browser.



![Choose New, Developer Services, Application Insights.](./media/app-insights-asp-net/16-page-views.png)



You'll also be able to write your own code to track how your users work with your app, right down to the detailed level of clicks and keystrokes.


#### Add Application Insights to your web pages


Get the code from the QuickStart blade of your Application Insights resource, and add it to your web pages:



![In your web app, open Quick Start and click 'Get code to monitor my web pages'](./media/app-insights-asp-net/02-monitor-web-page.png)



Add the code to a master page such as \_Layout.cshtml. Notice that it contains the instrumentation key that identifies your application resource.



[Learn more about web page tracking.](https://azure.microsoft.com/documentation/articles/app-insights-web-track-usage.md)


#### If your clients are device apps


If your application is serving clients such as phones or other devices, add the [appropriate SDK](https://azure.microsoft.com/documentation/articles/app-insights-platforms.md) to your device app.



If you configure the client SDK with the same instrumentation key as the server SDK, the two streams will be integrated so that you can see them together.


## Usage tracking


When you've delivered a new user story, you'd like to know how much your customers are using it, and whether they are achieving their goals or having difficulties. Get a detailed picture of user activity by inserting TrackEvent() and other calls in your code, both at the client and server.



[Use the API to track usage](https://azure.microsoft.com/documentation/articles/app-insights-api-custom-events-metrics/)


## Diagnostic logs


[Capture log traces](https://azure.microsoft.com/documentation/articles/app-insights-asp-net-trace-logs/) from your favorite logging framework to help diagnose any problems. Your log entries will appear in [diagnostic search](https://azure.microsoft.com/documentation/articles/app-insights-diagnostic-search/) along with the Application Insights telemetry events.


## Publish your app


If you haven't yet published your app (since you added Application Insights), do that now. Watch the data grow in the charts as people use your app.


### Keep separate resources for dev, test and release


For a major application, it's advisable to send telemetry data from debugging, testing and production into [separate resources](https://azure.microsoft.com/documentation/articles/app-insights-separate-resources.md).


## Add dependency tracking


[Dependency metrics](https://azure.microsoft.com/documentation/articles/app-insights-dependencies.md) can be invaluable to help you diagnose performance issues. They measure calls from your app to databases, REST APIs, and other external components.



In Diagnostic Search, select a request that failed or has a long duration. In the details blade, look under Calls to Remote Dependencies to see if the problem is in a call your app made to an external component.



![An example of a call to an external dependency with a long duration](./media/app-insights-asp-net/04-dependencies.png)



If you don't see anything listed, you need to follow some steps to set up dependency tracking.


#### If your app runs in your IIS server


Sign in to your server with admin rights, and install [Application Insights Status Monitor](https://go.microsoft.com/fwlink/?LinkId=506648).



(You can also use Status Monitor to [instrument an app that's already running](https://azure.microsoft.com/documentation/articles/app-insights-monitor-performance-live-website-now.md), even if it hasn't been built with the SDK.)


#### If your app is an Azure Web App


In the control panel of your Azure Web App, add the Application Insights extension.



![In your web app, Settings, Extensions, Add, Application Insights](./media/app-insights-asp-net/05-extend.png)



(The extension only assists an app that has been built with the SDK. Unlike Status Monitor, it can't instrument an existing app.)


## Availability web tests


[Set up web tests](https://azure.microsoft.com/documentation/articles/app-insights-monitor-web-app-availability/) to test from the outside that your application is live and responsive.



![Sample of web tests with some failed tests](./media/app-insights-asp-net/appinsights-10webtestresult.png)

