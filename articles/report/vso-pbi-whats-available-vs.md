<properties
	pageTitle="What's available in the Power BI Visual Studio Online connector"
  description="What's available in the Power BI Visual Studio Online connector"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 

# What's available in the Power BI Visual Studio Online connector


The Power BI data model for Visual Studio Online will continue to grow over the coming months to include data for more features.


## Currently available data


| Data | Details |
| --- | --- |
| Work Items | Current state, [trend data](https://msdn.microsoft.com/Library/vs/alm/Report/powerbi/create-trend-charts), and [rollup](https://msdn.microsoft.com/Library/vs/alm/Report/powerbi/create-rollup-charts) |
| Builds | XAML builds including build requests, queues and details |
| Source Control - Git | Commits, repositories, pull requests |
| Source Control - TFVC | Changesets, files, file changes and branches |


## Timeline for new data availability


| Data | Timeframe |
| --- | --- |
| Test Results | TBD |
| Work Item - Kanban | TBD |
| Work Item trend data and rollup  | September 2 |
| Work Item Current State | July 22 |
| Builds - XAML | June 24 |
| Source Control | May 27 |


## Work with the data model


The data model has several different sets of dimensions related to Team Foundation version control, Git, XAML builds and work items. These dimensions are described here along with their basic measures.


### General Purpose


| Dimension | Description |
| --- | --- |
| Dataset Details | Contains information on when the data in Power BI was last updated and the version of the Visual Studio Online connector data model being used. |
| Dates | Relates to pull requests (Create Timestamp) and work items (Created Timestamp). |
| Projects | Allows you to determine which project code check-ins and pull requests happened as well as serving as a filter against all work items. |
| Users | Detailed user information for use with work items, pull requests, changesets and commits. |


### Team Foundation version control


| Dimension | Description |
| --- | --- |
| Branches | Information on branches, including branch count. |
| Changesets | Information on changesets including (but not limited to) measures such as the count of changesets, changesets in the last 30 days, count of changesets by a given author. |
| File Changes | The type of change made against the file (add, change, delete) and associated measures. |
| Files | File path and extension information on checked-in files. |


### Git


| Dimension | Description |
| --- | --- |
| Commits | Information on commits such as the number of files added/deleted/edited, number of projects with commits and commit counts. |
| Pull Requests | Information on pull requests including age, count, authors and status. |
| Repositories | Information on the repos per project including name, count and by growth and commits. |


### XAML Builds


| Dimension | Description |
| --- | --- |
| Xaml Build Definitions | Build definitions including how the build is triggered. |
| Xaml Build Queues | Information build queues including if they are enabled and their status. |
| Xaml Build Requests | Information on build requests including build duration, percentiles, number of builds, how long the builds were queued for and retry reasons if the build failed. |
| Xaml Builds | All of the details regarding a build. This includes builds that failed and passed, error codes and messages, build quality and build durations. |


### Work Items


All individual work item tables have the following measures:


- Count of work items. This column name is the same as the table name. For example the Bugs table has a measure called "Bugs".
- Days in Proposed, Active, Resolved states for Median and 95th Percentile (except for the Product Backlog Items dimension).
- Whole days in Proposed, Active and Resolved states (except for the Product Backlog Items dimension). These measures are used for creating histograms of days in state.


Other tables may include measures specific to that work item type.



| Dimension | Description |
| --- | --- |
| Areas | Work item area name, path, level and individual area tree level. Can be used to slice or filter work items. |
| Bugs | Contains information relating to bugs and includes Effort, Original Effort, Remaining Work, Size and Story Points values. |
| Change Requests | Contains information relating to Change requests and includes the Original Estimate value. |
| Features | Contains information relating to Features and includes Business Value, Days Past Target and Days Until Target values. |
| Feedback Requests | Contains information relating to Feedback Requests. |
| Feedback Responses | Contains information relating to Feedback Responses. |
| Impediments | Contains information relating to Impediments. |
| Issues | Contains information relating to Issues and includes the Original Estimate value. |
| Iterations | Work item iteration name, path, level and individual iteration tree level. Can be used to slice or filter work items. |
| Product Backlog Items | Contains information relating to Product Backlog Items and includes Business Value and Effort values. |
| Requirements | Contains information relating to Requirements and includes Original Estimate and Size values. |
| Risks | Contains information relating to Risks and includes the Original Estimate value. |
| Tasks | Contains information relating to Tasks and includes Original Estimate, Completed Work and Remaining Work values. |
| Test Cases | Contains information relating to Test Cases. Please note that there is no test result data currently available in the Power BI model. |
| User Stories | Contains information relating to User Stories and includes the Story Points value. |
| Work Items | This dimension contains all work items, regardless of type. Work items in any table can be filtered or sub-divided by values in this dimension. The Work Items count in this table is an overall count and can be broken down using the Work Item Type field. This table contains all of the System.\* fields. |

