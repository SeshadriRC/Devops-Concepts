**Topics covered**

- Initialize a git repo
- what is .git file
- git clone vs git fork difference
- create a branch
- difference between git merge and git rebase

**commands**
```
git init
git status
git diff

git log
git log <branch-name>
git log --oneline       -> if you don't want to see lengthy log

git push
git remote -v
git remote add
git clone using https or ssh method authentication

git checkout -b <branch-name>
git checkout <branch-name>

git cherry-pick <commit-id>
git merge
git rebase

```

**1.  what is git init and .git file**

The video explains that git init is the command used to initialize a local Git repository (2:51). When you run git init, it creates a hidden folder called .git in your directory (4:09).

The .git folder is the key component of Git (4:11) and is responsible for:

- Tracking changes (4:14)
- Logging (4:17)
- Storing information like credentials for secure repositories (4:20-4:24)
- Allowing for hooks (e.g., pre-commit hooks) to prevent sensitive information from being pushed to Git (4:51-5:03).
- Essentially, .git enables Git to keep a track of everything, including versions and changes made to files

<img width="1172" height="550" alt="image" src="https://github.com/user-attachments/assets/eac2a7ba-5e36-4ae6-b007-bda502e32cba" />

---

**2. git diff**

git diff is a command used to see what changes have been made to a file (7:39-7:42). For example, if you add a new line of code, running git diff will show you exactly what has been added or changed in the file (7:42-7:51). It's useful for reviewing changes you've made, especially if you've made a lot and forgotten some

<img width="551" height="280" alt="image" src="https://github.com/user-attachments/assets/83c1852c-d62a-4614-9ea7-59ce7eb2a1a1" />

---

**3. git log**

- git log is a command that shows you a list of commits (10:32-10:34). It displays the history of changes, indicating who made a change and what the commit message was (11:15-11:22).
- If you're working in a team, git log helps you see who made which changes, which is crucial if something breaks and you need to identify the source of the issue
- By seeing the commit history, you can always go back to a specific working version of the code (11:08-11:12, 11:46-11:50).

<img width="827" height="212" alt="image" src="https://github.com/user-attachments/assets/59c17083-def3-4d2e-a16a-af38ec791155" />

---

**4. Git workflow used in an organization**

The presenter emphasizes that these three commands (git add, git commit, and git push) are used "day in day out" in organizations (13:31-13:36).

---

**5. Git push**

This command is used to upload your committed changes from your local repository to a remote Git repository (e.g., GitHub, Bitbucket) (12:25-12:30). This makes your changes accessible to teammates and integrates them into the shared codebase (12:39-12:59).

<img width="1193" height="654" alt="image" src="https://github.com/user-attachments/assets/b1578de6-08fa-4471-8c93-4a389182af1c" />

- why first git push not worked, its because we have created a repository using cli and there is no reference to the remote repository. we didn't configure a remote location. 
- However in the 2nd scenario , we have cloned it from remote. so automatically remote repository exists

---

**6. Git clone**

There are two methods

- HTTP
- SSH

**HTTP**

<img width="1182" height="332" alt="image" src="https://github.com/user-attachments/assets/cba46edc-1e21-49e6-955a-f7510f919847" />

**SSH**

- In the above pic you can see publich key, so just copy that PK and paste it in github

**settings** option in profile → SSH and GPG keys → Add new SSH key

<img width="1213" height="570" alt="image" src="https://github.com/user-attachments/assets/cd673ba3-04eb-4dc9-bf62-66217efba851" />
<img width="1219" height="387" alt="image" src="https://github.com/user-attachments/assets/b067dd4f-56cc-4bfc-9e55-8c120b5aa258" />
<img width="1188" height="544" alt="image" src="https://github.com/user-attachments/assets/66154feb-9f8a-4415-805b-ef9699170677" />


---

**7. git fork and git clone difference**


**git clone:**

**Purpose:** Used to download or pull a specific repository from a remote server (e.g., GitHub) to your local machine (19:07-19:14, 25:52-25:54).
**Action:** It creates a local copy of the repository (14:33-14:39).
**Use Case:** Typically used when you want to work on an existing project, either as a direct contributor or to simply get a local copy of the codebase (15:31-15:41).

**git fork:**

**Purpose:** Used to create a copy of a repository on the GitHub (or other Git hosting platform) server itself, under your own account (24:23-24:26, 25:50-25:52). Git is a distributed version control system, and forking leverages this by allowing you to create your own "replica" of a project (24:28-24:44).

**Action:** It creates a server-side copy of the entire repository at a specific point in time. This copy is independent of the original, meaning updates to the original repository will not automatically update your forked copy unless you explicitly pull those changes (25:00-25:06).

**Use Case:** Primarily used when you want to contribute to an open-source project or experiment with changes without directly affecting the original codebase. You make changes in your forked repository, and once confident, you can propose these changes back to the original project via a pull request (25:30-25:46). Many people create a fork to work on their own version of a project (24:51-24:58).

In essence, cloning is about getting a local copy to work on, while forking is about creating a server-side copy to enable independent development and collaboration (25:50-25:54).

---

**8. git branch**

<img width="428" height="141" alt="image" src="https://github.com/user-attachments/assets/e8b2f43a-5b23-4d9a-9d50-a4ca66737ed1" />


---

**9. git cherry-pick**

- below is the o/p of git log division

<img width="852" height="461" alt="image" src="https://github.com/user-attachments/assets/f60bd33b-b220-42a4-bfa8-f567c8197ba6" />

```
git cherry-pick <commit-id>
```

- git cherry-pick is a command used to selectively apply specific commits from one branch to another
- Cherry-picking is easy and convenient when you only need to bring over one or two specific commits from another branch
- git cherry-pick is not practical for large numbers of commits (e.g., "fifty thousand or sixty thousand commits"), as it would be time-consuming and prone to conflicts to manually cherry-pick each one


<img width="1177" height="622" alt="image" src="https://github.com/user-attachments/assets/ed32fdf4-95a3-4f6a-b7a5-002d8c989adc" />

- below is the o/p of git log main

<img width="1097" height="457" alt="image" src="https://github.com/user-attachments/assets/7935652a-5bc8-4edd-a796-a9c7793d7543" />


---
**10. git merge and git rebase**

- Note: We need to see both git merge and git rebase same time, then only we can able to understand

**git merge**

- added new functionality called multiplication

<img width="671" height="327" alt="image" src="https://github.com/user-attachments/assets/e4fd2c2e-e6b0-445e-841c-feeb04c2c3d1" />

- after doing git add, git commit. use the ```git log``` and see the below output. new commit is added called demonstrate merge

<img width="886" height="587" alt="image" src="https://github.com/user-attachments/assets/9447aadc-61ab-4f6d-b4ad-fab8134ff5c7" />

- ```git log mergeExample --oneline```

<img width="617" height="166" alt="image" src="https://github.com/user-attachments/assets/82ca517c-a2e2-4c7b-a81a-3afdb88a9ec5" />



**git rebase**

- created another branch for rebase and added functionality called percentage

<img width="544" height="322" alt="image" src="https://github.com/user-attachments/assets/849c4257-66c6-43ac-8794-d60639b06d0e" />

- after doing git add, git commit , check git log

<img width="906" height="566" alt="image" src="https://github.com/user-attachments/assets/ce6086fc-c25d-4ac6-a53d-af18368f954e" />

```git log ---oneline```
<img width="652" height="188" alt="image" src="https://github.com/user-attachments/assets/a6df40ed-1cc7-46f4-885c-f5329e84590a" />


**Now go to main**

- here also change something

<img width="466" height="300" alt="image" src="https://github.com/user-attachments/assets/05e94473-5a34-4138-a29c-3dd5fa077fc6" />

- then do git add, git commit

- Now merge with **mergeExample** branch

<img width="514" height="102" alt="image" src="https://github.com/user-attachments/assets/a114ddb4-2007-4e0a-a3a4-169d7db69ee5" />

- we supposed to commit here by giving ```wq!``` but somehow abi terminal not worked. so commit is unsuccessful

<img width="880" height="220" alt="image" src="https://github.com/user-attachments/assets/25feed69-61e3-40dd-8912-1cf46a04414e" />

<img width="1104" height="517" alt="image" src="https://github.com/user-attachments/assets/cc107f41-274a-4870-805a-f0fdb721c830" />

<img width="706" height="249" alt="image" src="https://github.com/user-attachments/assets/fd97871f-6736-4adb-806e-c0cf6d65db1b" />

- Now check the git log

<img width="997" height="623" alt="image" src="https://github.com/user-attachments/assets/9a3e10e4-3225-4015-9406-80976b55a929" />
<img width="991" height="650" alt="image" src="https://github.com/user-attachments/assets/660ce2ae-64b9-4100-858a-45db6b2603f6" />
<img width="997" height="623" alt="image" src="https://github.com/user-attachments/assets/f2c303bf-095e-4cd8-8068-1090b515a927" />

- Now merge with **rebaseExample** branch

  - here we got merge conflict, we cleared it

    - merge conflict occurred because the same file (calculator.sh) was changed in different branches simultaneously by multiple people (43:12-43:40).

    Specifically, in the practical demonstration, a conflict arose because:

       - One branch added a "percentage" functionality. Another branch added a "multiplication" functionality.
         
    - how to handle merge conflicts, stating that you typically need to "sit with the developers" to decide which changes to keep or how to integrate them, before adding and committing the fixed file (43:46-44:39).
    - so after fixing the merge conflict , we need to add and commit again or do ```git rebase --continue```
      

<img width="559" height="453" alt="image" src="https://github.com/user-attachments/assets/cdffaf6b-310f-4bb4-9297-7c2a71a308e2" />

<img width="959" height="655" alt="image" src="https://github.com/user-attachments/assets/6070a456-b268-45ac-a491-752393200deb" />

<img width="936" height="475" alt="image" src="https://github.com/user-attachments/assets/9413705d-b838-4a2c-af36-62726c798603" />

(or)

<img width="966" height="328" alt="image" src="https://github.com/user-attachments/assets/7288adb7-7c74-4fab-bd7c-afaaca9429fb" />


<img width="824" height="648" alt="image" src="https://github.com/user-attachments/assets/aff03e89-8b7d-4238-a661-bccef9992057" />

- now finally we can see **mergeexample** is coming at the top and **rebasexample** coming in between

<img width="1204" height="689" alt="image" src="https://github.com/user-attachments/assets/4736cfef-462d-4b5e-b9c1-e25a09c242e2" />

- Just to understand, Below is the steps we followed before

<img width="787" height="310" alt="image" src="https://github.com/user-attachments/assets/db8f52bb-9a6b-40d6-90ec-69018060b2f3" />

---
**11. difference between git rebase and git merge**

- merge and rebase will do the same thing, it will merge both the branches
- if you want to maintain linear history then use ```git rebase```
- if you don't bother about that then use ```git merge```. so with the merge we don't get linear commit history. so all the changes will come and get created at the top
- so if you see below image deomonstrate merge and percentage modified same timing and after that only test commit done at master. But you can see merge is showing at top, not maintaining linear history, however rebase maintaining the history. note the timings

  <img width="886" height="629" alt="image" src="https://github.com/user-attachments/assets/c3c5d717-279c-4363-9677-8b247a22bba6" />
