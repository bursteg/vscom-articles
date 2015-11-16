<properties
	pageTitle="Track test status"
  description="Track test status"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 

# Track test status


Quickly view the status of your testing using lightweight charts. 
For example, find out how many test cases are ready to run,
or how many tests are passing and failing in each test suite. 
You can pin these charts to your home page, then all the team 
can see the progress at a glance.



![On the Charts tab, view test plan status with charts that you created](./media/track-test-status-vs/OverviewTrackResults.png)


## Track testing progress


Use test results charts to track how your testing is going. 
Choose from a fixed set of pre-populated fields related to results.
By default, a pie chart is created for each test plan. 
This chart is grouped by the outcome field to show the latest results
for all the tests in the test plan.



View this default chart from the Charts tab.



![Select test plan. Go to Charts tab to view default chart](./media/track-test-status-vs/DefaultChart.png)



Add your own charts for test results to visualize what's important 
for your team. If you already know how to add a chart, jump to the 
[examples](https://www.visualstudio.com/get-started/test/track-test-status-vs#TestResultsExamples) below of charts that you can create.


1. Select the test plan or test suite for your chart in the 
Test plan tab. Then create a new chart.



![On the Charts tab; click New. Select New Test Result Chart](./media/track-test-status-vs/NewTestResultChart.png)
2. Select the chart type. Based on the chart, configure the 
fields that you want to use to group by, or for rows and columns.



![Name your chart. Select the field values. To save, click OK](./media/track-test-status-vs/ConfigureChart.png)



All charts roll up the information for any child test suites 
of the test plan or test suite that you selected.
3. Save the chart. Now it will be displayed in the charts tab 
for the test plan or test suite that you selected.





### Test results examples


**What's the test status for a specific test suite?**



Select the test suite from the Test plan tab and add 
a test results pie chart. Group by outcome.



![On the chart tab, choose New test result chart; choose Pie chart. In Group By, select Outcome](./media/track-test-status-vs/ExampleOutcome.png)



**What's the test status for user stories that my team's testing this sprint?**



If you have created requirement-based test suites in your test
plan for your user stories, you can create a chart for this.


1. Group these requirement-based test suites together 
in a static test suite.
2. Select this static test suite in the Test plan tab.
3. Add a test results stacked bar chart. Choose Suite 
as the rows pivot and Outcome as the columns pivot.



![For Rows, select Suite. For Columns, select Outcome. To save, click OK](./media/track-test-status-vs/ExampleUserStories.png)


**How many tests has each tester left to run?**



Select your test plan from the Test plan tab and add a test 
results pivot table chart. Choose Tester as the rows pivot and
Outcome as the columns pivot.



![For Rows, select Tester. For Columns, select Outcome. To save, click OK](./media/track-test-status-vs/ExampleTesterTestsLeft.png)



**How can I check quality based on the configuration?**



Use either a stacked bar chart or a pivot table chart. 
Choose Configuration as the rows pivot and Outcome as 
the columns    pivot.



**How can I track why tests are failing for my team?**



For failure analysis, use either a stacked bar chart 
or a pivot table chart. Choose Tester for the rows 
and Failure type for the columns. (Failure type for 
test results can only be set using Microsoft Test Manager.)



**How can I track the resolution for failing tests for my team?**



For resolution analysis, use either a stacked bar chart 
or a pivot table chart. Choose Tester for the rows and 
Resolution for the columns. (Resolution type for test 
results can only be set using Microsoft Test Manager.)


## Track test case status


Use test case charts to find out the progress of your 
test case authoring. The charts for test cases give 
you the flexibility to report on columns that you add 
to the Tests tab. By default, test case fields are not 
added to the view in the Tests tab.



If you already know how to add a chart, jump to the
[examples](https://www.visualstudio.com/get-started/test/track-test-status-vs#ExamplesTestCase) below of charts that you can 
create for test cases.


1. Add any fields you want to use for your test case chart 
from the Tests tab with Column options. Then the fields will 
appear as choices in the drop-down lists for grouping for 
your test case charts.
2. Select the test plan or test suite for your chart in 
the Test plan tab. Then add a test case chart.



![Test hub: select test suite; Charts tab; New test case chart](./media/track-test-status-vs/NewTestCaseChart.png)



All charts roll up the information for any child test suites 
of the test plan or test suite that you selected.
3. Select the chart type. Based on the chart, configure the 
fields that you want to use to group by, for rows and columns,
or the range (trend charts only).



![Choose the chart type; choose the fields for the chart](./media/track-test-status-vs/ConfigureChart2.png)



You can't group by test suite for the test case charts.
4. Save the chart. Now it will be displayed in the charts 
tab for the test plan or test suite that you selected.





### Test case examples


**How can I track burndown for test case creation?**



Use a stacked area trend chart to view the burndown for 
how many test cases are ready to be run. Choose State 
for the stack by field and Ascending for the sort field.



![Create a stacked area chart: For Stack By, choose State, then sort by ascending value](./media/track-test-status-vs/ExampleBurndownReadiness.png)



**How can I track burndown for automation status?**



Use a stacked area trend chart to view the burndown 
for how many test cases have been automated. Choose 
Automation status for the stack by field and Ascending 
for the sort field.



**If multiple teams own test cases in my test plan, can I see how many each team owns and the priorities of the tests?**



If your teams are organized by area path, then your can use a 
test case pie chart. Choose Area path for the group by field.



If you want to know the priorities of these tests, then create 
a stacked bar chart. Choose Area path for rows and priority
for the columns.



**How can I track test creation status by team members?**



Test case owners are tracked by the Assigned to field. 
Use a stacked bar chart or a pivot table chart. Choose 
Assigned to for rows and status for the columns.


## Try this next

- [Control how long to keep test results](https://www.visualstudio.com/get-started/test/how-long-to-keep-test-results)

## Q&amp;A

#### Q:  Can I view the recent test results for an individual test case?


A:  Yes, select the test case within a test suite and then 
choose to view the test details pane.



![From test suite, select test case. On toolbar, click test details icon to view the test details pane](./media/track-test-status-vs/ShowDetailsPane.png)



View the recent test results for this test case.



![In test details pane, open the Pane list, choose Test Results](./media/track-test-status-vs/TestResultsPane.png)


#### Q:  How is data shown in the charts for test cases that are in multiple test suites?


A:  For test case charts, if a test case has been added to 
multiple test suites in a plan then it's only counted once.



For test result charts, each instance of a test that is run 
is counted for each of the test suites separately.


#### Q:  Who can create charts?


A:  You need at least a Basic license to create charts.


#### Q:  How can I share the team's test status with all my stakeholders?


A:  Pin a chart to your team's home page for all the team to view. 
Use the chart's context menu.



![Open the chart](./media/track-test-status-vs/EditDeletePinChart.png)



You must be a team administrator to do this. Even team members with 
stakeholder licenses can view the test charts on the home page. 
Learn more about the 
[home page](https://msdn.microsoft.com/library/jj920199.aspx). 
Or learn more about
[team administration](https://msdn.microsoft.com/library/hh409274.aspx).


#### Q:  How can I edit or delete a chart?


A:  Select the option you want from the chart's context menu.


#### Q:    How do I control how long I keep my test data?


A:  [Learn more here](https://www.visualstudio.com/get-started/test/how-long-to-keep-test-results).
