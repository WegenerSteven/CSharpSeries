# setup GitHub

1. Create an account at **[github.com](https://github.com/)**
2. Optionally install **[GitHub Desktop](https://desktop.github.com/download/)** for visual commits and sync
3. Authenticate and link GitHub Desktop with your account

---

### Core Git Workflow

| Step | Command                          | Description                     |
| ---- | -------------------------------- | ------------------------------- |
| 1    | `git init`                       | Initialize a new Git repository |
| 2    | `git add .`                      | Stage files for commit          |
| 3    | `git commit -m "Initial commit"` | Save a snapshot                 |
| 4    | `git status`                     | View changes and staging info   |
| 5    | `git branch feature-login`       | Create a branch                 |
| 6    | `git checkout feature-login`     | Switch branches                 |
| 7    | `git merge feature-login`        | Merge changes into main         |
| 8    | `git push origin main`           | Push commits to GitHub          |
>"Commits are cheap" do them often
- `git clone:` Clone an existing repository
```bash
    git clone <repository-url>
```


