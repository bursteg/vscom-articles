<properties
	pageTitle="Develop and share your code in TFVC using Visual Studio"
  description="Develop and share your code in TFVC using Visual Studio"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 

# Develop and share your code in TFVC using Visual Studio


Whether your software project is large, small, or brand new, 
in most cases you'll be better off if you use version control 
as early as possible. 
Here, we'll show you how to get started with 
Team Foundation Version Control (TFVC), a centralized system.
If you want to work in a distributed system, 
you can instead use [Git with Visual Studio Online](https://www.visualstudio.com/get-started/code/share-your-code-in-git-vs).



Is your code in another place? [Learn how to migrate it here](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs#migrate).


## Open your team project in Visual Studio

1. Before you start, if you haven't already:


 - [Sign up and create your team project](https://www.visualstudio.com/get-started/setup/sign-up-for-visual-studio-online).
 - Install [Visual Studio 2013 or later](http://go.microsoft.com/fwlink/?LinkId=309297).
2. Go to your team project's page 
(`http://{youraccount}.visualstudio.com/DefaultCollection/{yourteamproject}`)
and then open Visual Studio to connect to your team project.



![On your team project overview page, click Open in Visual Studio](./media/share-your-code-in-tfvc-vs/GoHomeOpenInVisualStudio.png)
3. Sign in to Visual Studio Online from Visual Studio. 
[Why is my sign-in page different than when I sign in to Visual Studio?](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs#DifferentSignInPage)





## Configure your workspace

1. In Visual Studio, configure your workspace.



![On Team Explorer home page, click Configure Workspace](./media/share-your-code-in-tfvc-vs/ConfigureWorkspace.png)



[I don't see the Configure Workspace link. What do I do next?](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs#workspace_exists)
2. Confirm your workspace path, map your workspace, and get the source.



![On Team Explorer home page, click Map and get](./media/share-your-code-in-tfvc-vs/MapAndGet.png)
3. Now you can check in source, queue builds, and manage work.



![Visual Studio is now connected to your team project](./media/share-your-code-in-tfvc-vs/MapWorkspaceSuccess.png)

## Create a new app


If you already have an app that you want to add to version control,
skip down to [Add an existing app](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs#app_add).



![New solution from team explorer](./media/share-your-code-in-tfvc-vs/team-explorer-new-solution.png)



Now that you've added your app, you can skip down to 
[snapshot your code](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs#snapshot).






## Add an existing app

### Move and open the solution

1. Close the solution.
2. Open the workspace folder that you created when you [configured your workspace](https://www.visualstudio.com/get-started/code/share-your-code-in-tfvc-vs#workspace).



![Open the workspace folder from source control explorer](./media/share-your-code-in-tfvc-vs/open-workspace-folder-from-source-control-explorer.png)
3. Move the code you want to upload to the workspace folder.



![Move your source code to your workspace folder](./media/share-your-code-in-tfvc-vs/IC689415.jpg)
4. Open your solution in Visual Studio.



![Open your solution in Visual Studio](./media/share-your-code-in-tfvc-vs/open-solution-from-team-explorer-home.png)

### Add the solution to Visual Studio Online

1. Open the solution explorer (Keyboard: Ctrl + Alt + L).
2. Add your solution to version control.



![Add the solution to Visual Studio Online](./media/share-your-code-in-tfvc-vs/IC682953.png)
3. Check in the solution.



![Check in your solution](./media/share-your-code-in-tfvc-vs/IC682954.png)
4. Add a comment and check in.



![Add a comment and check in pending changes](./media/share-your-code-in-tfvc-vs/IC685248.png)
5. Open the source control explorer.



![Open the source control explorer](./media/share-your-code-in-tfvc-vs/IC682140.png)



Your solution is now in TFS.



![Your solution in the source control explorer](./media/share-your-code-in-tfvc-vs/IC689416.png)


Your whole team can work on the code now. All your changes are tracked in version control.






## Snapshot (check in) your code

1. When you edit code in Visual Studio, the changed file is automatically checked out. For example, Site.css is checked out after the border color has been changed to #ddd.



![Checked out file in the team explorer](./media/share-your-code-in-tfvc-vs/IC682155.png)
2. Compare the modified file with the latest version in source control.



![Compare in the solution explorer's context menu](./media/share-your-code-in-tfvc-vs/IC682955.png)



You can see the difference between the two versions.



![Compare window](./media/share-your-code-in-tfvc-vs/IC682157.png)
3. Check in the changes.



![Check in from the context menu in the solution explorer](./media/share-your-code-in-tfvc-vs/IC682956.png)



You can also check in from the code window, or the team explorer.
4. If you're working on a task or fixing a bug that's tracked as a work item, add that work item to your pending changes. Source control will resolve the bug or close the task, and it'll link the changeset to the work item.



![Related work items in pending changes](./media/share-your-code-in-tfvc-vs/IC682159.png)
5. Add a comment and check in.



![Source control explorer, source file context menu, check in](./media/share-your-code-in-tfvc-vs/IC685249.png)
6. Open the source control explorer.



![Source control explorer in the team explorer home page](./media/share-your-code-in-tfvc-vs/IC682161.png)
7. View the history of the file you changed.



![Source control explorer, source file context menu, view history](./media/share-your-code-in-tfvc-vs/IC682957.png)



All the changesets that include this file are listed.



![History window](./media/share-your-code-in-tfvc-vs/IC682163.png)

## Try this next


[Get your code reviewed](https://www.visualstudio.com/get-started/code/get-code-reviewed-vs)


## Q&amp;A

#### Q: My code is somewhere else. Can I migrate it to my TFVC project on Visual Studio Online?


A: Yes:


- [Upgrade From Visual SourceSafe](https://msdn.microsoft.com/library/ms253060).
- [Migrate from your on-premises Team Foundation server](https://www.visualstudio.com/get-started/setup/migrate-team-projects-vs).





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






#### Q:    I don't see the Configure Workspace link shown in the steps above. What do I do next?


A:    You might already have a workspace on your computer. To see your workspace, open Source 
Control Explorer. Or change your workspace. Find out how to [manage files under 
source control](https://msdn.microsoft.com/library/ms181370.aspx) or 
[manage workspaces](https://msdn.microsoft.com/library/ms181383.aspx).



![In Team Explorer, click Source Control Explorer or Manage Workspaces](./media/share-your-code-in-tfvc-vs/OpenSCE_ManageWorkspaces.png)
