<properties
	pageTitle="Share your code in Git using Eclipse"
  description="Share your code in Git using Eclipse"
  services="visual-studio-online"
  documentationCenter = ""
  authors="terryaustin"
  manager="terryaustin"
  editor="terryaustin" /> 


# Share your code in Git using Eclipse





Share your code with your team with Visual Studio Online and Eclipse.







Before you start:





1. If you don't have a Visual Studio Online account, [create it first](../setup/sign-up-for-visual-studio-online.md).

2. If you have not yet connected to a team project in your Visual Studio Online account, [do that now](../setup/connect-to-visual-studio-online.md).





If your team project uses Git in your Visual Studio Online account, read on. However, if your team project uses TFVC in your Visual Studio Online account,then read [Share your code in TFVC using Eclipse](share-your-code-in-tfvc-eclipse.md)













## Share using Git



### Clone the repository



1. Show the Git views.







![Windows menu, show window, other](./media/share-your-code-in-git-eclipse/show-git-views.png)







Select the repositories and staging views.







![Show view dialog box, Git expanded, Git Repositories and Git Staging selected](./media/share-your-code-in-git-eclipse/git-views-selected.png)







If you don't have the Git views, you can get them by [downloading EGit](http://www.eclipse.org/egit/).

2. Use the Git repositories view to clone the Git repository for your team project.







![Clone a Git repository link in the Git Repositories view](./media/share-your-code-in-git-eclipse/clone-git-repository.png)

3. Specify the URL for your project repository. The URL will look like `http://{your_account}.visualstudio.com/DefaultCollection/_git/{your_team_project}`





 - [Find out your repo URL](share-your-code-in-git-eclipse.md#gitrepourl).

 - Create a [personal access token](share-your-code-in-git-eclipse.md#pat) for authentication. 
Enter your usual username and use the token as the password.





![Clone Git Repository dialog box with a team project URL and personal access token provided](./media/share-your-code-in-git-eclipse/clone-repo-dialog.png)

4. Specify where you'll keep the cloned repository on your machine. It's okay if your Git repository is empty.







![Local destination dialog box](./media/share-your-code-in-git-eclipse/local-destination.png)







The repository for your team project shows up in the Git repositories view.







![Git repositories view showing the cloned repository](./media/share-your-code-in-git-eclipse/cloned-repository.png)



### Push your code to the remote repository



1. In Package Explorer, right-click the project and choose Team, Share Project.







![In the Package Explorer, the project's context menu, Team, Share Project](./media/share-your-code-in-git-eclipse/share-project.png)

2. Make sure you share it to Git.







![Share Project dialog box with Git selected](./media/share-your-code-in-git-eclipse/share-project-git.png)







Map the remote repository to your working directory.







![Configure Git Repository dailog box](./media/share-your-code-in-git-eclipse/configure-git-repository.png)

3. Add your files to the Git index to stage your changes.







![Git staging view, unstaged changes context menu,  Add to Git Index](./media/share-your-code-in-git-eclipse/add-to-git-index.png)

4. Enter a commit message and push the source to the remote repository.







Use your [personal access token](share-your-code-in-git-eclipse.md#pat) for authentication.







![Commit and Push button in the Git Staging view](./media/share-your-code-in-git-eclipse/commit-and-push.jpg)





Your code is in your team project's Git repository, so now your teammates can contribute.





### Try this next



- [Build your Eclipse projects](../build/build-your-app-eclipse.md)



## Q&amp;A



#### Q: Where can I find the URL for my Git repository?





A: You'll find it in the code hub in your team project.





1. Sign in to your Visual Studio Online account and browse to your team project or type the team project URL directly in your browser.



- The URL will look like `https://{your_account}.visualstudio.com/DefaultCollection/{your_team_project}`

- If you are not sure about your team project URL, [Sign in to your Visual Studio](http://go.microsoft.com/fwlink/?LinkID=309329) and select your account.



1. Open the code hub from your you team project's home page.







![Team project home page, code explorer](./media/share-your-code-in-git-eclipse/code-explorer.png)

2. Select the the repository and click on the **clone** action to get the URL.







![Team project home page, code explorer, clone selected to show the URL](./media/share-your-code-in-git-eclipse/clone-url.png)



#### Q: Why should I use personal access tokens?





A: Personal access tokens are a more convenient and secure replacement 
for alternate authentication credentials.













#### Q: Why can't connect to my Git repo?





A: To use Git with your Visual Studio Online account, create a personal access token 
so that you can sign in from Eclipse.





1. Sign in to your Visual Studio Online account (`http://[youraccount].visualstudio.com`).

2. Go to your team project's home page and open your profile.







![Team project home page, my profile](./media/share-your-code-in-git-eclipse/my-profile.png)

3. Create a new personal access token for this account.







![Add a personal access token on the security page ](./media/share-your-code-in-git-eclipse/add-personal-access-token.png)

4. Enter the details for this token.







![Enter token details](./media/share-your-code-in-git-eclipse/setup-personal-access-token.png)

5. Select the [scopes](https://www.visualstudio.com/integrate/get-started/auth/oauth#scopes) that this token authorizes.







![Select scopes for this token](./media/share-your-code-in-git-eclipse/select-personal-access-token-scopes.png)

6. After you finish creating the token, make sure to copy the token. You'll use this token as your password for your Git tools or application.







![Use token as password for your git tools or application](./media/share-your-code-in-git-eclipse/create-personal-access-token.png)







**Note: Remember that these tokens are your identity. 
When used, the token is acting as you. 
Keep your tokens secret and treat them like your password.
To help keep your token more secure, consider using the 
[Windows Credential Store for Git](http://gitcredentialstore.codeplex.com)
so that you don't have to enter your credentials every time you push.**







For example, if you use the Git command prompt to run a Git command, you'll be prompted for a username and password.





```

git clone https://[account].visualstudio.com/DefaultCollection/_git/[team project]

```





Enter a username that does not contain an @ character (for example, Jamal, not fabrikamfiber4@hotmail.com). 
Use the token that you created as your password.





```

Username for 'https://fabrikam-inc.visualstudio.com': Jamal
Password for 'https://fabrikam-inc.visualstudio.com': [COPY THE TOKEN HERE]

```

7. When you don't need your token anymore, just revoke the token to remove its access from this account.



#### Q: Can I still use alternate authentication credentials?





A:  Yes.





1. Sign in to your Visual Studio Online account (`http://[youraccount].visualstudio.com`).

2. Go to your team project's home page and open your profile.







![Team project home page, my profile](./media/share-your-code-in-git-eclipse/my-profile.png)

3. Enable alternate authentication credentials for this account. Then provide a secondary username and password.







![Enable alternate authentication credentials link on the user profile page](./media/share-your-code-in-git-eclipse/enable-alternate-credentials.png)



#### Q: What if the Git views don't show up.





A: You can [download EGit](http://www.eclipse.org/egit/) to use Git with Eclipse.





#### Q: Can I use my GitHub repository instead of Visual Studio?





A:  Yes, provide the name of your GitHub repository in Step 3 under "Clone the repository" above instead of the name of your VSO repository.

