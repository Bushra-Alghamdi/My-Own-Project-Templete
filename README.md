Project Name
------------

### Project Description
- Please add a description of your project/game

### Team & Roles
- Please add a list of team members

### Task Tracking & Project Management
- Please link your tasks board here



---

### To Do 
**Add Team members to the repo** 
- Add your teammates to have "Write" access to the repository through the repository [Settings/access](../../settings/access).
  - Settings -> Manage Access -> Invite teams or people
  - Add your teammates by their GitHub username.
  - You may create a team instead of adding people individually.
  - https://docs.github.com/en/github/administering-a-repository/managing-repository-settings/managing-teams-and-people-with-access-to-your-repository
  
**Setup CodeOwners for the Rewiew Process** 
- Update the [CODEOWNERS](.github/CODEOWNERS) file as needed.  
  - Please leave "@gamechangers-sa/reviewers  @gamechangers-sa/leads" as reviewers but you can add to that list.
  - See https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-on-github/about-code-owners

**Create the initial Unity 3D Project**
- Open Unity Hub, Select New→ 3D 
  - Name the Project “3D Flight Demo” or something similar so we can keep track of projects.
  - Create the project inside the folder that was created during the git clone process above.
- If Unity adds the project into a sub-folder, you MUST either
  - Copy/paste the .gitignore file to the project sub-folder, or
  - Cut the project files from the sub-folder and paste them into the project root folder.
  - Not doing either of these will add all of the unnecessary build, output, and log files to the repo.
    - This causes bloat and costs money for unnecessary storage and bandwidth. 
- Commit the changes and push them to GitHub
  - We are still working on main but that is OK for the initial commit.
  - `git add .` - I know I keep saying “Do NOT use git add . and then keep telling you to use it.
    - It is bad practice, but if you set up your ignore files correctly it can be “ok”.
  - `git commit -m “creating project”`
  - `git push`

**Branch Protection Rules** 
- Discuss the workflow strategy with your teammates to decide what is best for the project. 
- Review: [GameChangers Confluence: Introduction to GitHub Desktop Pull Requests Workflow](https://gamechangers.atlassian.net/wiki/spaces/GAMECHANGE/pages/122191873/Introduction+to+Github+Desktop+Pull+Requests+Workflow).  
  - Set up Branch Protection Rules in [settings/branches](../../settings/branches) or Settings -> Branches -> Add rule
    - Set the following settings:
      - *Branch name pattern*: `main` - this tells GitHub to match any branches that have “main” and apply the rule.
      - Check: *Require pull request reviews before merging*  
      - Check: *Require review from Code Owners*  
    - If you plan to add tests immediately, 
      - Check the *Require status checks to pass before merging* and *Require branches to be up to date before merging* boxes.
      - Add "Run Edit Mode Tests" and "Run Play Mode Tests" in the "Search" bar.
  - See the following for more information
    - https://docs.github.com/en/github/administering-a-repository/defining-the-mergeability-of-pull-requests/about-protected-branches
    - https://docs.github.com/en/enterprise-server@3.0/github/administering-a-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule
    ![GitHub Branch Protection](https://github.com/gamechangers-sa/gamechangers-sa/blob/main/documentation/img/git-branch-protection.png)  

**Collaboration Board / Task Management** 
- Set up a collaboration board and team tasks in the [Projects](../../projects) tab and click *Create a project*  
  - You may use Jira or Trello as well.   
    ![GitHub Projects](https://github.com/gamechangers-sa/gamechangers-sa/blob/main/documentation/img/git-task-management-1.png)  
- Name the board “Tasks” or something similar.
- For the *Project Template*, select *Automated kanban with reviews*.
  ![GitHub Projects](https://github.com/gamechangers-sa/gamechangers-sa/blob/main/documentation/img/git-task-management-2.png)


**Set up Git LFS - on each team members computer** 
- Initialize [git-lfs ](https://www.atlassian.com/git/tutorials/git-lfs)
  - Using the git-bash terminal window you used to clone the repository, run the command `git lfs install`. 
    - If it is successful, you will see.
     ```
    $ git lfs install
    > Git LFS initialized.
    ```
    - If it is unsuccessful, download git lfs from [https://git-lfs.github.com/](https://git-lfs.github.com/). Run the downloaded executable and try the above command again.
  - See [Installing git lfs](https://docs.github.com/en/github/managing-large-files/versioning-large-files/installing-git-large-file-storage)

**Update the Project Readme**
- Update the fields listed above regarding your project name, game descritption, team members & roles, task board.
- Quality project documentation is extremely important and helps with project and team organization.
  - Poor documentation increases bad development habits; increases poor organization, and both of these lead to failed teams, projects, and companies.
  - We call concepts Best, Good, or Bad “Practices”, because these items take practice; we need to do them over and over again to help give ourselves and our projects the best chance of success.
  - **Good habits start now.**
    - But, bad habits also start now; so we need to pick which ones we want to practice. 
    - Games and software are already unstable and bad enough as it is, we don’t need to add to this.
- Delete the To-Do list section after completing the steps.
