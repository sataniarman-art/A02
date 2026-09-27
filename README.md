# Introduction to Git, WebStorm, and GitHub

This introduction to Git, WebStorm, and GitHub is for those who are new to using these tools.

In this tutorial, you will learn how to install and configure Git, WebStorm, and GitHub, and how to use them in concert to manage a project. It is written so that even someone with no experience in the field can follow it from end to end.

## Part 1: Directions on Using WebStorm

1. **Download and install Git.** To connect to GitHub, you should install the Git command-line tool on your computer, as WebStorm's version control functionality is implemented on top of the Git command-line tool.
   - Go to the official Git downloads page: https://git-scm.com/downloads
   - Select your operating system (Windows, macOS, or Linux). Your operating system is automatically detected, and you will get the appropriate installer.
   - Run the downloaded installer.
   - During installation on Windows, accept the default settings unless otherwise specified, and check that **Git Bash** is checked (it provides a terminal for running Git commands).
   - On macOS, you can also use Homebrew (`brew install git`) to install Git.
   - Check that the install was successful by opening a terminal (or Git Bash) and typing:

     git --version

     A version number should be shown, for example, `git version 2.51.0`.
   - Configure your identity — the one Git will associate with each commit you make:

     git config --global user.name "Your Name"
     git config --global user.email "your.email@example.com"


2. **Download and install the WebStorm IDE.**
   - Go to the official WebStorm page: https://www.jetbrains.com/webstorm/
   - Click **Download**. It's recommended to install via the Toolbox App (https://www.jetbrains.com/toolbox-app/), which lets you install, update, and manage multiple JetBrains IDEs from a single location.
   - Run the installer for your operating system and follow the setup wizard, using the default installation settings.
   - WebStorm is free for non-commercial use and has a 30-day free trial for commercial use. Students can also get a free license with a valid school email address at https://www.jetbrains.com/community/education/.
   - Launch WebStorm. On first open, you can select a UI theme (Light or Darcula) and install any recommended plugins.

3. **Create a GitHub account.**
   - Sign up at https://github.com/.
   - Enter your email address, password, and username, then check your email to verify.
   - After signing in, you will have your own account that can hold its own repositories.

4. **Create a New Project in WebStorm.**
   - Start WebStorm and choose **New Project** from the Welcome screen.
   - Select a project type (or "Empty Project" for an empty folder), select a location on your computer, and click **Create**.
   - The project opens in WebStorm's main editor window.

5. **Turn the Project into a Git Repository.**
   - Go to **VCS > Create Git Repository** in WebStorm's top menu.
   - Select the root folder of your project and confirm.
   - The folder is now tracked with Git. In the Project panel, file names change color to indicate their Git status (e.g., red for untracked, green for newly added).

6. **Make the first commit.**
   - Create or edit a file, such as `README.md`, in your project.
   - Go to **Git > Commit** (or press `Ctrl+K` on Windows/Linux, `Cmd+K` on Mac).
   - In the Commit panel, make sure the box beside the file(s) to include is checked.
   - Write a clear commit message describing the change (see commit message style below).
   - Click **Commit** to save the snapshot to the local repository, or **Commit and Push** to commit and push to GitHub at the same time.

7. **Create a Repository on GitHub and connect it.**
   - On GitHub, click the **+** in the upper-right corner and select **New repository**.
   - Give it a name, optionally enter a description, select **Public** or **Private**, and click **Create repository**.
   - Copy the HTTPS URL from the repository's green **Code** button.
   - Back in WebStorm, click **Git > Manage Remotes** and add the GitHub URL as your `origin` remote — this connects your local repository with the one on GitHub.
   - Alternatively, use **VCS > Import into Version Control > Share Project on GitHub**, and WebStorm will create the repository and connect it for you automatically, provided you've already signed in with your GitHub account in WebStorm (**Settings > Version Control > GitHub**).

8. **Push your code to GitHub.**
   - Go to **Git > Push** (or `Ctrl+Shift+K` / `Cmd+Shift+K`).
   - Review the commits to be pushed, then click **Push**.
   - Refresh your repository page on GitHub — you should now see your files there.

9. **Pull changes from GitHub.** If you or a teammate modified anything on GitHub (or on another computer), update your local work:
   - Go to **Git > Update Project** (or `Ctrl+T` / `Cmd+T`).
   - WebStorm fetches and merges (pulls) and updates your local files.

### Step 10: Work with Branches

- Let's click on the branch name in the bottom right corner of WebStorm window.
- Click on New Branch, give it a name (e.g. feature/navbar), and hit Enter. WebStorm checks you out on the new branch.
- Do the same with your changes, commit them and push them up to GitHub.
- Open a Pull Request on GitHub to request the merge of your branch into the main branch and have another teammate or yourself review the changes before they're merged.

### Step 11: Resolve a Merge Conflict

When two branches made the same changes to the same lines of a file, Git can't automatically merge them:

- After a pull or merge WebStorm will identify the file with conflicts in red with a conflict icon.
- Right click the file and select "Git > Resolve Conflicts", or click on the notification that appears.
- The three pane merge tool appears in WebStorm, displaying the three versions: yours, the resulting and "their" version.
- Select the lines to retain (or edit the result pane directly), and click Apply.
- Commit the file that has been resolved to complete the merge.

### Commit Message Style

Commit messages should be short, specific, and start with a type of change:


Task: Create Repository
Fixed: resolved a minor issue with GitHub use that was causing some bugs.
Fix: changed README.md for definition of terms


## Part 2: Glossary

- **Branch**: An independent line of development in a repository that lets you make changes without impacting the main line of code until you're ready to merge those changes.
- **Clone**: To make a complete local copy of a remote repository – including its commit history and all files.
- **Commit**: To save a snapshot of a project's changes, which is recorded with a message explaining the changes.
- **Fetch**: Download new commits, new branches or new tags from a remote repository without merging them in your local repository.
- **GIT**: A distributed version control system (DVCS) that is free and open source and is used to track changes to files and coordinate the work of multiple individuals.
- **GitHub**: A web-based service for hosting Git repositories with some collaboration features like pull requests, issues and project boards.
- **Merge**: Including changes from one branch in another branch.
- A conflict that occurs when Git cannot automatically merge changes because the same lines in a file have been changed in different ways on different branches, and must be resolved manually.
- **Push**: Option to upload the local commits to a remote repository that others can access.
- **Pull**: Fetch a change from the remote repository and merge it into your local repository (a fetch and a merge).
- **Remote**: A copy of a repository that is stored in another location (e.g., on GitHub) that is accessible to your local repository via push and pull.
- A place to store and keep track of all files and changes of a project; also known as a "repo.

## References

Git. (n.d.). *Git downloads*. Retrieved September 26, 2026, from https://git-scm.com/downloads

GitHub. (n.d.). *Quickstart for repositories*. GitHub Docs. Retrieved September 26, 2026, from https://docs.github.com/en/repositories/creating-and-managing-repositories/quickstart-for-repositories

JetBrains. (n.d.). *WebStorm*. Retrieved September 26, 2026, from https://www.jetbrains.com/webstorm/

JetBrains. (n.d.). *Share a project on GitHub*. WebStorm Help. Retrieved September 26, 2026, from https://www.jetbrains.com/help/webstorm/github.html

JetBrains. (n.d.). *JetBrains Toolbox App*. Retrieved September 26, 2026, from https://www.jetbrains.com/toolbox-app/

JetBrains. (n.d.). *Free educational licenses*. Retrieved September 26, 2026, from https://www.jetbrains.com/community/education/