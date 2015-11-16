
# Create and run unit tests with Visual Studio


Create unit tests and run them frequently to make sure your code is working properly.


## Create a unit test

1. Create a unit test project.



![Add a unit test project to your solution](./media/create-and-run-unit-tests-vs/createunittest1.png)
2. Name your project.



![Unit test project template](./media/create-and-run-unit-tests-vs/createunittest2.png)



The project is now added to your solution.



![Unit test project in Solution Explorer](./media/create-and-run-unit-tests-vs/createunittest5.png)
3. In the unit test project, add a reference to the project you want to test.



![Add a reference to your unit test project](./media/create-and-run-unit-tests-vs/createunittest6.png)
4. Select the project that contains the code you'll test.



![Select the reference to add](./media/create-and-run-unit-tests-vs/createunittest7.png)
5. Code your unit test.



![Add code to your unit test](./media/create-and-run-unit-tests-vs/createunittest8.png)

## Run unit tests

1. Open Test Explorer.



![On the Test menu, open Test Explorer](./media/create-and-run-unit-tests-vs/rununittest1.png)
2. Run unit tests.



![Run unit tests in Test Explorer](./media/create-and-run-unit-tests-vs/rununittest2.png)



You can see the unit tests that passed or failed in Test Explorer.



![Review unit test results in Test Explorer](./media/create-and-run-unit-tests-vs/rununittest3.png)

## Try this next

- [Debug your app](https://www.visualstudio.com/get-started/code/debug-your-app-vs)

## Q &amp; A

#### Q:    Can I run unit tests in Visual Studio if I use a different unit test framework?


A:  Yes, use the plug-in for that framework so that Visual Studio's test runner 
can work with that framework. Here are the 
[unit testing framework plug-ins for Visual Studio](http://go.microsoft.com/fwlink/?LinkID=246630) 
that are available right now.


1. Use Visual Studio's extension manager to download your plug-in.



![Select 3rd-party unit test plug-ins with extension manager](./media/create-and-run-unit-tests-vs/install3rdpartyunittestframeworks1.png)
2. Download your plug-in from the Visual Studio Gallery under Tools/Testing, 
or search for it if you know the name.



![Download your plug-in](./media/create-and-run-unit-tests-vs/install3rdpartyunittestframeworks2.png)
3. Create a class library project.



![Create a class library project](./media/create-and-run-unit-tests-vs/create3rdpartyunittest1.png)



Add the project to your solution.



![Name the class library project and add it](./media/create-and-run-unit-tests-vs/create3rdpartyunittest3.png)
4. In the class library project, run NuGet to install the plug-in.



![Manage NuGet packages to install the plug-in](./media/create-and-run-unit-tests-vs/create3rdpartyunittest3a.png)



[NuGet](http://nuget.codeplex.com/documentation) is an extension of Visual Studio 
that you can use to add and update libraries and tools for your projects.
5. Install your plug-in. If you know the name, you can search for it online.



![Install your 3rd-party framework](./media/create-and-run-unit-tests-vs/create3rdpartyunittest4.png)



The framework is referenced in your project.



![The reference for the 3rd-party unit test framework is added into your solution](./media/create-and-run-unit-tests-vs/create3rdpartyunittest6.png)
6. In the class library project, add a reference to the project you want to test.



![Add a reference to the project](./media/create-and-run-unit-tests-vs/createunittest6.png)
7. Select the project that contains the code you'll test.



![Select the code project for you to test](./media/create-and-run-unit-tests-vs/createunittest7.png)
8. Code your unit test.



![Add code to your unit test](./media/create-and-run-unit-tests-vs/create3rdpartyunittest7.png)
