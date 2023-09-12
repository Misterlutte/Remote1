![logo](1color-lightbg@2x.png)
# Work with git
## 1. Check if git is installed
In terminal enter the command: 
```Bash 
  git --version
```
If **git** is installed then git version text will appear, if it's not installed than error massage will appear

## 2. Git instalation
[Download](https://git-scm.com/book/ru/v2/%D0%92%D0%B2%D0%B5%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%A3%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-Git) the latest git version. Install **git** with default settings

## 3. Git setup
For the first time using **git** you have to introduse yourself:
```Bash
  git config --global user.name "<Your_name>" use english latters 
  git config --global user.email "<email_adress@email.com>"
```

## 4. Initialization of the repository
To start working with **git** you have to enter 
```Bash
  git init
```
in **terminal** (it will create **.git** folder in your main folder)

## 5. Writing the change to the repository 
While working, you sould save your progress, for this you have to enter
```Bash
  git add + <folder_name> 
  git commit -m "<changes description>"
```

## 6. View commit history
To view your commits history and **commit codes** you have to enter
```Bash
  git log
```
## 7. Moving between saves
To moving between your saves (*commits*) you have to enter 
```Bash
  git checkout commit_code <---- more functions than just (swich)
or
  git switch commit_code <---- only (swich) function
 ```
**commit code** - watch 6th paragraph

## 8. How to ignore file
 To exclude tracking files in the repository, you need to create a **folder** called **.gitignore** in the repository and write there the file names or patterns corresponding to such files. **My example**:

* Create a `.gitignore`  
* ![screen](screen.jpg)

* Unload your picture in repozitory:

* ![screen](screen3.jpg) 

* ![screen](screen2.jpg) <---- In **VS CODE**

## 9 Creating branches in **git**
Default branch name in **git** is - `master`

To create new branch you need to enter a command:

```Bash
  git branch <new branch_name>
```
## 10. Merging branches and resolving conflicts
To merge the **selected branch** with the current one enter the command:
```Bash
  git merge <selected_branch_name>
```
If the same part of the file was changed in **both branches**, then when they are merged, a conflict may arise that requires **user** participation.

 * ![alt](palapa.jpg)

 The solution to the conflict is shown in the **picture above**.
 
 Here are all the possible solutions:
 1. Accept current change (master branch)
 2. Accept incoming change (selected brunch)
 3. Accept both changes (both variants on a screen and you may fix both by your hands)
 4. Compare changes (shows you a screen with difference between two branches watch on (**picture below**))

* ![url-adress](https://learn.microsoft.com/en-us/visualstudio/version-control/media/vs-2022/git-compare-branches.png?view=vs-2022#lightbox)
This solutions from **VS CODE**

## 10. Deleting branches
If you don't need specific **branch** any more than you may delite it by using command:
```Bash
  git branch -d <branch_name_you_wanna_delite>
```
* You can't delite **current** branch! Because you are on this branch 
* You can't delite **merged** branch! Because **unmerged branch** include **commits** that are not reachable from any of your branches.
