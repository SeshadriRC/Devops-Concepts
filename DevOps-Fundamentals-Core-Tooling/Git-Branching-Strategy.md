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
-> main branch (also called master or trunk)
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
                                                                                                                                                                                                                                                   ~main → feature → merge to main → release → test → ship
→ If urgent issue: main → hotfix → fix → merge back to main and release
