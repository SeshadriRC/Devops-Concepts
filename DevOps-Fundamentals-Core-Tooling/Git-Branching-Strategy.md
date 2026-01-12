**Summarize**

- What is branch in github
- master branch
- feature branch
- Release branch
- hotfix branch

<img width="1011" height="628" alt="image" src="https://github.com/user-attachments/assets/e8b63ab5-b33e-4fe5-84ec-0b0f74e1bdcf" />

---

**youtube comments summarized**


**Git Branching Flow – Summary **
→ main branch (also called master or trunk)
→ Holds the stable, production-ready code. Always up-to-date.

**Feature branch**
→ Created from main to develop a new feature or a breaking change.
→ Developers collaborate here independently.
→ Example: feature/login-auth.

**Merge**
→ Once the feature is complete and tested, the feature branch is merged into main.
→ Optionally, the branch is deleted after merging to keep the repo clean.

**Release branch**
→ Created from main when preparing for a production release.
→ Used for final testing, bug fixes, and polishing before deployment.
→ Example: release/v1.0.

**Ship/Deploy**
→ Code from the release branch is deployed to production.
→ Release is tagged for versioning (e.g., v1.0.0).

**Hotfix branch**
→ Created directly from main when an urgent bug or critical issue occurs in production.
→ After the fix, it's merged into both main and release branches.  
                                                                                                                                                                                  main → feature → merge to main → release → test → ship
                                                                                                                                                                                  
→ If urgent issue: main → hotfix → fix → merge back to main and release


---

**AI summarized Uber example**

the video uses Uber as an example to illustrate the concept of branching in Git and how new features are integrated (5:13).

Here's how the Uber example is used:

Initial State (Cab Application): Imagine Uber started solely as a cab booking application, with its code hosted on GitHub. This existing, functional code base represents the main or master branch (16:45).

Introducing a New Feature (Bikes): When Uber decided to introduce "bikes" as a new service, developers weren't confident if adding this functionality directly to the existing cab code would affect its stability. So, they created a new branch called feature bikes from the main codebase (5:51, 17:29).

Parallel Development and Testing: A team of developers worked on the feature bikes branch, adding and testing the new bike functionality without disturbing the live cab application (6:08, 17:37). Meanwhile, active development and fixes continued on the master branch for the cab service (17:47).

Merging the Feature: Once the "bike" functionality was fully developed, tested, and deemed stable, the feature bikes branch was merged back into the master branch (6:16, 18:21). This combined the existing cab features with the new bike features into a single, updated codebase. The feature bikes branch was then deleted (6:23, 18:24).

Subsequent Features (Intercity): The process repeats for other major features, like introducing "Intercity" travel. A new branch, feature Intercity, would be created, developed, and eventually merged back into the master branch (18:37).

Releases: When a new version of the Uber application (e.g., "release V3") is ready for customers, a release branch is created from the then-current master branch. This release branch undergoes final testing, and once stable, it's shipped to customers (19:10, 19:38).

This example demonstrates how branching allows for parallel development of new features, bug fixes, and releases without compromising the stability of the live production environment.
