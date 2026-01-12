**Topics covered**

- Initialize a git repo
- what is .git file
- git clone vs git fork difference

**commands**
```
git init
git status
git diff
git log
git push
git remote -v
git remote add
git clone using https or ssh method authentication
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



