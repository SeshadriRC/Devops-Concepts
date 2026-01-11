[video](https://www.youtube.com/watch?v=fIMySI_gZJU&list=PLdpzxOOAlwvIc1TjTwopNSjRJkzES2ZXk&index=12&t=384s)

**summarize**

- what is git
- centralized version control and distributed version control system
- git and github difference
- git commands
- creating a git repository in UI
  


---

**commands**

```
git init    -> initialize a git repo

```

- lifecycle commands of git

```
git add
git commit
git push
```

- diff

```
git diff
```

- log

```
git log
```

- reset

```
git reset --hard <commit-id>
```
---

**Interview ques**

1. Difference between centralized version control system and distributed.

Below are **short, clear, interview-ready questions and answers** (no extra theory).

---

## 1️⃣ What is Git?

**Answer:**
Git is a **distributed version control system** used to track changes in source code, manage versions, and allow multiple developers to collaborate efficiently.

---

## 2️⃣ What is a Version Control System (VCS)?

**Answer:**
A Version Control System is a tool that **records changes to files over time** so that specific versions can be recalled, compared, or restored.

---

## 3️⃣ What is a Centralized Version Control System (CVCS)?

**Answer:**
A Centralized Version Control System has **one central repository** where all code is stored, and developers must connect to this server to get or commit changes.

**Examples:** SVN, CVS, Perforce

**Key Points:**

* Single point of failure
* Requires network connection
* Limited offline work

---

## 4️⃣ What is a Distributed Version Control System (DVCS)?

**Answer:**
A Distributed Version Control System allows **each developer to have a complete copy of the repository**, including full history, on their local machine.

**Example:** Git

**Key Points:**

* No single point of failure
* Works offline
* Faster operations

---

## 5️⃣ Is Git centralized or distributed?

**Answer:**
Git is a **Distributed Version Control System (DVCS)**.

---

## 6️⃣ Difference between Centralized and Distributed VCS (Interview Table)

| Feature      | Centralized VCS       | Distributed VCS (Git) |
| ------------ | --------------------- | --------------------- |
| Repository   | Single central server | Local + remote copies |
| Offline work | Not possible          | Possible              |
| Speed        | Slower                | Faster                |
| Failure risk | High (single point)   | Low                   |
| Examples     | SVN, CVS              | Git                   |

---

## 7️⃣ Why is Git preferred over centralized VCS?

**Answer:**
Git is preferred because it is **fast, supports offline work, provides better branching and merging, and has no single point of failure**.

---

## One-line summary (very useful)

> **Git is a distributed version control system where every developer has a full copy of the repository, unlike centralized systems that rely on a single server.**

If you want, I can also give **2–3 follow-up Git interview questions** commonly asked after this.

<img width="1531" height="916" alt="image" src="https://github.com/user-attachments/assets/2ab2d581-3dbf-4ee9-a804-9038bfe2bf1f" />

<img width="684" height="804" alt="image" src="https://github.com/user-attachments/assets/bb249175-a99e-4e4f-9de3-07c9ca8ce6bf" />

****************************************************************************************************************************

Below is a **short, crisp, interview-ready answer**.

---

## Difference between Git and GitHub

### 1️⃣ What is Git?

**Answer:**
Git is a **distributed version control system** used to track code changes and manage source code history locally.

---

### 2️⃣ What is GitHub?

**Answer:**
GitHub is a **cloud-based platform** that hosts Git repositories and provides collaboration features like pull requests, issues, and CI integration.

---

## Key Differences (Interview Table)

| Feature       | Git                  | GitHub                             |
| ------------- | -------------------- | ---------------------------------- |
| Type          | Tool                 | Platform / Service                 |
| Purpose       | Version control      | Repository hosting & collaboration |
| Works offline | Yes                  | No (needs internet)                |
| Installation  | Installed locally    | Web-based                          |
| Ownership     | Open source          | Owned by Microsoft                 |
| Commands      | git init, git commit | pull request, issues (UI features) |

---

## Interview One-Liner (Very Important)

> **Git is the tool that tracks code changes, while GitHub is a platform that hosts Git repositories and enables team collaboration.**

---

## Simple analogy (optional if interviewer asks)

> **Git is like a camera that records changes, GitHub is like Google Drive where you store and share those recordings.**

If you want, I can also give **Git vs GitLab vs Bitbucket** in the same interview format 👍

****************************************************************************************************************************


- once if we give git init, then after that if u type ```ls -a``` then ```.git``` will show. if we delete ```.git``` then it won't get tracked

<img width="1339" height="521" alt="image" src="https://github.com/user-attachments/assets/c46eb5c1-17db-4e75-a583-d9f29100764b" />

- Everything in git is tracked as objects, that is where object is used . eg: calculator.sh

<img width="1082" height="493" alt="image" src="https://github.com/user-attachments/assets/9c38faed-99fe-46f1-9404-820861ef3947" />

- hooks are used in Git to prevent unintentional commits, such as committing passwords or API tokens (20:21-20:36). They essentially allow you to set up actions that trigger automatically at certain points in the Git workflow.

- config is used to configure your Git credentials, such as setting up secure Git repositories that require secrets, TLS, or certificates
  
- ```git diff```

<img width="828" height="328" alt="image" src="https://github.com/user-attachments/assets/ab8b9449-871f-4fac-a416-3a0c1325068c" />

- below we can see git is tracking objects

<img width="1108" height="565" alt="image" src="https://github.com/user-attachments/assets/c699bd02-acc8-487e-9b09-96cb853a3398" />

- git log

<img width="764" height="327" alt="image" src="https://github.com/user-attachments/assets/e08306a4-1260-4921-98e7-4ec142aeee14" />

- now your project manager is telling you to go back to previous version, so from git log we need to find that particular commit and then do git reset

<img width="1048" height="160" alt="image" src="https://github.com/user-attachments/assets/9c08418c-6f46-498a-b6d3-3907f8f169e8" />

- suppose we need to share this code with our peers, or with organization then we need to use github or self hosted git or bitbucket, this is where distributed is coming into picture

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dacde82b-1db5-49fc-b591-eea2141f7c09" />
