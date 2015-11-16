<properties
	pageTitle="Build your Eclipse projects"
  description="Build your Eclipse projects"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 

# Build your Eclipse projects


Build your Java projects in the cloud with Ant, Gradle, or Maven and Visual Studio Online.


## Set up your build

1. If you haven't already:


 - [Connect Eclipse to your Visual Studio Online account](../setup/connect-to-visual-studio-online.md).
 - [Upload the code](../code/share-your-code-in-git-eclipse.md) that you're going to build.
2. From the team explorer in Eclipse, open the builds page.



![Builds in the Team Explorer home page](./media/build-your-app-eclipse/team-explorer-home.png)
3. Create a build definition.



![New Definition link in the team explorer builds page](./media/build-your-app-eclipse/new-build-definition.png)
4. Choose Start with an empty build definition.



![Empty build definition template](./media/build-your-app-eclipse/start-with-an-empty-build-definition.png)
5. If your project builds with Maven, add the Maven build step. Otherwise add the build step your team uses.



![Add build step](./media/build-your-app-eclipse/add-build-step.png)



![Add Maven build step](./media/build-your-app-eclipse/add-build-step-maven.png)
6. Provide the path to your Maven POM file.



![Maven build step](./media/build-your-app-eclipse/maven-build-step.png)
7. Select the continuous integration (CI) trigger and specify the code you want to build.



![CI trigger](./media/build-your-app-eclipse/build-trigger-ci-master-batch.png)
8. Save the definition.



![Save button](./media/build-your-app-eclipse/build-definition-save-button.png)



![Save dialog box](./media/build-your-app-eclipse/build-definition-save-dialog-box.png)
9. Queue your new definition to make sure it works.



![Queue the build](./media/build-your-app-eclipse/queue-build-dialog-box-with-hosted.png)



![Completed build](./media/build-your-app-eclipse/eclipse-build-completed.png)


You've created your first Eclipse build in the cloud! Since this is a CI build, a build is started every time you push a commit to one of the branches specified on the Triggers tab.


## Try this next

- [Create a backlog](../work/create-your-backlog-vs.md) to plan, organize, and track your work.
- [Add users and their licenses](../setup/assign-licenses-to-users-vs.md) to your Visual Studio Online account.

## Q &amp; A

#### Q: Can I set up gated builds?


[Improve code quality with branch policies](https://msdn.microsoft.com/Library/vs/alm/Code/git/branch-policies) with an option to require that code builds before it can be merged to a branch.
