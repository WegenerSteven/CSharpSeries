# introduction


Welcome to our first session of the **CSK Mentorship Program (Web Track)**!  
In this session, we’ll learn the foundations of **Git** and **GitHub**, the essential tools every developer must master before building real-world projects in **C#/.NET**.

> By Shikhule benard
---

## 🧠 What You’ll Learn
By the end of this session, you should be able to:
- Understand what Git and GitHub are, and why they matter.
- Set up Git on your local machine.
- Create repositories and manage code versions.
- Collaborate using branches and pull requests.
- Connect your local Git repo to GitHub.

---

## 🔍 1. What is Git?
**Git** is a **version control system** — a tool that tracks changes in your code over time.  
Think of it as a “timeline” for your project — you can move back and forth between versions, merge updates, and work with others without losing anything.
It was created by **Linus Torvalds in 2005** and is maintained by **Junio Hamano**.

### Why Use Git?
Git allows developers to:
- Track and manage changes in code over time.
- Work collaboratively without overwriting each other’s work.
- Revert to previous versions when something breaks.
- Create branches to experiment safely with new ideas.

> “Git is your project’s time machine.” – Xiao Li, *University of Zurich, Git & GitHub Tutorial*:contentReference[oaicite:0]{index=0}


---

## ☁️ 2. What is GitHub?
**GitHub** is a cloud web-based platform where you can host Git repositories online.  
It enables you to:
- Backup your code.
- Share projects publicly or privately.
- Collaborate using pull requests and code reviews.
- Contribute to open-source.

### GitHub allows you to:
1. **Host** repositories (public or private)
2. **Collaborate** with your team using branches and pull requests
3. **Contribute** to open-source projects via forks

---

👉 In simple terms:  
**Git** is the tool.  
**GitHub** is the place you use the tool to collaborate.

---

> Reference: [Kelcho Spense Git Tutorial](https://kelcho-spense.github.io/Learning-git/readme.html)  
> Source: *GitHub and Something Else*, Lic. Fauricio Alban Conejo Navarro:contentReference[oaicite:1]{index=1}

---

## ⚙️ 3. Setting Up Git
### Installation (Windows)
1. Go to [git-scm.com/downloads](https://git-scm.com/downloads)
2. Download and install Git.
3. Verify installation:
   ```bash
   git --version
4. Configuration
After installation, se tup your identity:
```bash
    git config --global user.name "Your Name"
    git config --global user.email "Your Email"
```
> Use *global* to set the username and e-mail for every repository on your computer.

