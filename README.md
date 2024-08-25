# GIT

Git/Github is a fantastic tool that facilitates developers to look up in their code at any point of time.

> Ohh, git and github are similar terms and can be used in palce of each other?

Umm...Sorry! My mistake. It's an old habit I am trying to get rid of. 
**Git and Github are not same.**

First of all, I would discuss about the so called **Git** and further about **Github**. Still wondering that they are same? No, they are not.

## What is Git ?

Git is a tool which allows us to use certain commands and these commands enable us to travel back in time in our code 
**Stress that - It is a tool.** 
You can think of it as a *time machine* using which we can travel from one point of time to other.
So, in case of time travel we have *time*; analogusly in case of code travel we have ***check points***.

**Check Points :** These are the breaks in the code which we mark time to time (usually when a sub-part of code is completed). We can use them
to travel back and forth in our code base. Since, I am explaining the topic, how can I left it without an example. 

    Lets take three years 2020, 2024 and 2027. Here, 2020 is past, 2024 is present and 2027 is future.
    Now if we want to travel in time using time machine (git in our case). we can go to 2020 for past, 
    and 2027 for future. So, what are these years, these are the check points only. These check points
    are enabling us and working as a unit of time so that we can travel past and future in our code.

In git's langauge, the folders are called as *repository*.

You know **Git is Open-Source**.

Further, I will discuss about various commands that git provides us.

## Various Git Commands

1. **git init :** This command is used to initialize a new repository in our local folders.
2. **git add :** This command is used to stage the files and folders before getting them ready to be pushed into the repository.
     > git add . for stashing all the files and folders.
     > git add <file name> to stash a particular file or folder.
3. **git commit :** This command takes a snapshot or you can say a exact copy of the code that are staged to push.
     > git commit -m "message" : This is the way of using the command. We have to provide a commit message
     > before commiting. This message usually consists of what the committed code is doing.
4. **git push :** This command finally pushes the committed code in the repository keeping track of the area of the changes.
     > git push origin <branch> : This is how the command is used, <branch> is a term which denotes another another
     > snapshot of the whole codebase running paralley. It is a part of the main code only.

     > git push --set-upstream <branch> : This command is used to set an upstream branch. It means whenever we try
     > to push the code just by simply writing git push, the code will be pushed in the <branch> only.

### Branch related operation
Creating branch is an operation in git, it is used when we don't want to spoil or effect the main codebase due to our changes.
Making branch just creates a copy of the main codebase in which the made changes won't affect the main code base.
Following are the commands to perform operation related to branches:

1. **git branch :** To know the list of the branches and current branch. The current branch is marked using a '*'.
2. **git checkout -b <branch> :** Created a new branch from the current branch and also switches you to the new branch.
3. **git switch <branch> :** This switches you to another branch without creating a new branch.
   
   ![image](https://github.com/user-attachments/assets/7afa7470-3fdf-4891-bcec-b49036e87e13)

4. **git branch -D <branch> :** This deleted the mentioned branch. To delete a particular branch, you have to switch to a
   another one first.
5. **git merge <branch> :** This is use to merge two branches. The <branch> here is the branch we want to merge into the current branch. The commit history of both the branches is also merged. After using this command, you may encounter a merge conflict which is a common thing that I'll discuss later.
6. **git rebase <branch> :** This also merges two branches. The <branch> here is the branch we want the current branch to merge into. The commit history is also merged. After using this command, you may encounter a rebase conflict which is a common thing that I'll discuss later.

   > Heyyy.. the definitons for git merge and git rebase are exactly same. Then why two different names to the single operation.

   Wait wait! I don't write stupid things. There is a difference. **The difference is in how the commit histories of both the branches are merged.**

       Again! Lets take an example.
       Suppose I made two branches say A and B. I made two commit in branch A at 1 o clock and other at 3 o clock. I made one commit in branch B at 2 o clock.
       Now if I use git merge to merge B into A, the commit history will be like 1 2 3. If I use git rebase to rebase B into A, the commit history will be like
       1 3 2.
   
   Exactly! This is the amazing difference.

   In rebasing, one branch is merged on the top of the other unlike merging.

### Commit related operations
Making commits means making checkpoints in the code so that we can revisit the portion of the code if required in future.
Below are the commands related to commits:

1. **git commit -m "message" :** This is used to commit the staged changes.
2. **git log :** It opens the whole commit history with the commit blob.
3. **git checkout <commit hash> :** We can go to a particular commit.
4. **git commit --amend -m "message" :** This is used to change the commit message.
5. **git show <blob> :** This show the information about various git objects.

## Conflicts in git
So, as I mentioned earlier, you may get conflicts while merging and rebasing so they are called as merge conflict and rebase conflict respectlively. But these are not done. There are more conflicts:

1. **Merge conlfict :** This conflict occurs while merging branches when different code comes to the same line of a file.
2. **Rebase conflict :** This conflict occurs while rebasing branches. Rest is same as merge conflict.
3. **Revert conflcit :** Reverting means undoing the changes made in a particular commit. This conflict occurs when we revert a part of the code, which is related to the commit that was made later.
4. **Cherry-Pick Conflict :** Cherry-picking means making a change in a commit from one branch to another. This conflict occur while cherry-pickiing if the changes made in one branch conflict with the other.

   So this one make it clear what is the end result of merging:|)
   
   ![image](https://github.com/user-attachments/assets/e719fefa-0715-4b1c-be60-05c4e23dc37a)

There are few more but less encoubntere and less relevant. 

### How to resolve a conflict?
A conflict is denoted using "<<<<", ">>>>" and "===" in the conflicting area. So, we just have to remove these to resolve a merge conflict.

## GitHub
Yeeyyyy! Finally we are here. 
GitHub is a web-based platform that provides hosting for version control using Git. It is widely used for software development and collaboration, enabling multiple people to work on projects simultaneously. 
Hence, **Git is a tool, github is a website that host git**.

Well, at the end I will only say - Using git and github is cool :)

![image](https://github.com/user-attachments/assets/c1161e3d-f772-494a-91a4-0db0518d3f36)

Thanks for reading.
