<properties
	pageTitle="Develop and share your code in Git using Visual Studio"
  description="Develop and share your code in Git using Visual Studio"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 

# Develop and share your code in Git using Visual Studio


Whether your software project is large, small, or brand new, 
in most cases you'll be better off if you use version control 
as early as possible. Here, we'll show you how to get started with 
Git, a distributed system. If you want to work in a centralized system, 
you can instead use [TFVC with Visual Studio Online](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs).


## Open your team project in Visual Studio

1. Before you start, if you haven't already:


 - [Sign up and create your team project](https://www.visualstudio.com/get-started/setup/sign-up-for-visual-studio-online).
 - Install [Visual Studio 2013 or later](http://go.microsoft.com/fwlink/?LinkId=309297).
2. Go to your team project's page 
(`http://{youraccount}.visualstudio.com/DefaultCollection/{yourteamproject}`)
and then open Visual Studio to connect to your team project.



![On your team project overview page, click Open in Visual Studio](./media/share-your-code-in-git-vs/GoHomeOpenInVisualStudio.png)
3. Sign in to Visual Studio Online from Visual Studio. 
[Why is my sign-in page different than when I sign in to Visual Studio?](https://www.visualstudio.com/get-started/code/share-your-code-in-git-vs#DifferentSignInPage)

## Clone your repository

1. Clone the repository onto your dev machine.



![Choose Clone Repository](./media/share-your-code-in-git-vs/IC684063.png)
2. Store the repository locally.



![Choose Clone to store the repository locally](./media/share-your-code-in-git-vs/IC682931.png)

## Create a new app


If you don't already have an app in the repo, create one.


1. Create a new project.



![New solution from team explorer](./media/share-your-code-in-git-vs/team-explorer-git-new-solution.png)
2. Choose a template and add the new code project to version control.



![Choose a template](./media/share-your-code-in-git-vs/IC687148.png)

## Confirm your settings and add the app

1. On the changes page (Keyboard: Ctrl + 0, G), if you haven't already done it,
confirm your user name and email address.



![Configure settings from the changes page](./media/share-your-code-in-git-vs/confirm-git-settings-from-changes-page.png)



![Confirm the default settings](./media/share-your-code-in-git-vs/git-initial-settings-with-default-values.png)
2. Add a comment and commit your app to version control.



![Add app to version control on Changes page](./media/share-your-code-in-git-vs/team-explorer-git-changes-add-app.png)

## Snapshot (commit) your code


With your code project stored in a local Git repository on your dev machine, 
you can commit as early and as often as you like.


1. As you write your code, your changes are automatically tracked by Visual Studio. 
You can commit one or more specific changes to your local repository from Solution Explorer
(Keyboard: Ctrl + Alt + L).



![When your changes are ready, select Commit](./media/share-your-code-in-git-vs/IC683030.png)
2. On the Changes page, add a comment and then commit your changes.



![Add a comment and choose Commit](./media/share-your-code-in-git-vs/IC683031.png)



These changes are now committed.



![Your changes are now committed](./media/share-your-code-in-git-vs/IC683032.png)

## Pull changes from your team


Pull changes on a regular basis to ensure your code integrates well with the latest code from the team.


1. From the commits page (Keyboard: Ctrl + 0, O), fetch the commits to see any changes that your team has made.



![Choose Fetch to see any changes that your team has made](./media/share-your-code-in-git-vs/IC682939.png)
2. When you're ready, pull these commits into your local repository.



![Choose Pull to get these commits locally](./media/share-your-code-in-git-vs/IC682942.png)
3. The changes from your team are now integrated in your local repository.



![The changes are now integrated](./media/share-your-code-in-git-vs/IC682943.png)

## Push your local commits to the server


When the code you've written on your dev machine is ready, you can push your changes from your local Git repository to the team project.


1. From the changes page (Keyboard: Ctrl + 0, G), make sure you've committed your changes.



![Commiting from the Changes page](./media/share-your-code-in-git-vs/IC682975.png)
2. Go to the commits page (Keyboard: Ctrl + 0, C).



![Push changes](./media/share-your-code-in-git-vs/IC682976.png)
3. Push your changes.



![Push changes](./media/share-your-code-in-git-vs/IC682977.png)

## Q&amp;A

#### Q: Why is my sign-in page different than when I sign in to Visual Studio?


A:    Your sign-in page depends on whether you used a Microsoft account or 
work account with Visual Studio Online. So, sign in with the username and 
password that you used with Visual Studio Online.


#### Q:    Why doesn't Visual Studio launch when I click "Open in Visual Studio" on my team project page?


A:    This link requires [Visual Studio 2013](http://go.microsoft.com/fwlink/p/?LinkId=254509) 
or later. It doesn't launch earlier versions of Visual Studio.


#### Q:    Can I use earlier versions of Visual Studio to connect to Visual Studio Online?


A:    Yes, you can use Visual Studio 2013 or 2012. You can also use Visual Studio 2010, 
but you'll need to install [Service Pack 1](https://www.microsoft.com/download/details.aspx?id=23691) 
and [KB2662296](http://support.microsoft.com/kb/2662296) first. Or, you can use Visual 
Studio 2008 SP1, with [this GDR update](http://support.microsoft.com/kb/2673642). 
Launch Visual Studio, then connect to Visual Studio Online using your account URL, 
and select your team project.


#### Q: How can I see what I've changed?


A: To see what you've changed, compare your changes with the last commit.



![Choose Compare with Unmodified from the context menu](./media/share-your-code-in-git-vs/IC685270.png)


#### Q: How can I get more information about the commits from my team before I pull them?


A: Sometimes you need to see the details about incoming commits from your team. That way you can understand how a change will integrate with your work.



![Choose View Commit Details](./media/share-your-code-in-git-vs/IC682940.png)



You can get details on the changes to each file.



![Choose Compare with Previous from the context menu](./media/share-your-code-in-git-vs/IC685291.png)


#### Q: How do I associate my changes with related work items?


A: From the changes page you can run a query, and then drag a work item into the list of related work items.



![Associating a work item on the Changes page](./media/share-your-code-in-git-vs/IC685315.png)


#### Q: Can I use Git command-prompt tools?


A: Yes. See [Use Git from the command prompt](https://msdn.microsoft.com/Library/vs/alm/Code/git/command-prompt).


#### Q: Where can I learn more?


A: [Use Visual Studio and Team Foundation Server with Git](https://msdn.microsoft.com/en-us/Library/vs/alm/Code/git/overview)
