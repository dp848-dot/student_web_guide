# Git — Getting Started

**Why Git?**  
Git is the tool developers use to track changes, collaborate, and manage code. You'll use it every day!

### Prerequisites

- **Mac:** Terminal app, Homebrew recommended.
- **Windows:** WSL2 (Ubuntu or similar), Git installed.
- **GitHub account** (or similar).

### Install Git

**Mac (Homebrew):**
```sh
brew update
brew install git
```

**WSL2 (Ubuntu):**
```sh
sudo apt update
sudo apt install git -y
```

**Verify installation:**
```sh
git --version
```

### Configure Git

Set your name and email:
```sh
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Set VS Code as your editor (optional):
```sh
git config --global core.editor "code --wait"
```

### SSH Keys for GitHub

**Mac:**
```sh
ssh-keygen -t ed25519 -C "you@example.com"
eval "$(ssh-agent -s)"
ssh-add -K ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

**WSL2:**
```sh
ssh-keygen -t ed25519 -C "you@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```
Copy the output and add it to your GitHub SSH keys.

### Basic Workflow

Clone a repository:
```sh
git clone git@github.com:username/repo.git
cd repo
```

Check status and history:
```sh
git status
git log --oneline --graph
```

Make changes:
```sh
git add filename
git commit -m "Describe your change"
git push origin main
```

Pull updates:
```sh
git pull
```

### Branching

Create a new branch:
```sh
git checkout -b feature/my-feature
```

Push your branch:
```sh
git push -u origin feature/my-feature
```

### Useful Commands

- `git status` — See changes
- `git add <file>` — Stage changes
- `git commit -m "message"` — Save changes
- `git push` — Upload changes
- `git pull` — Download updates
- `git checkout -b <branch>` — New branch

### Troubleshooting

- **Detached HEAD?**  
  `git checkout main`
- **Merge conflicts?**  
  Edit files, `git add`, then `git commit`
- **Undo last commit:**  
  `git reset --soft HEAD~1`
- **Revert a pushed commit:**  
  `git revert <commit>`

### Resources

- [Pro Git Book](https://git-scm.com/book/en/v2)
- [GitHub Docs](https://docs.github.com/en)
- [Learn Git Branching (interactive)](https://learngitbranching.js.org/)

---

## Next Steps

- Practice: Set up SSH, clone a repo, create a branch, commit, push, and open a Pull Request.
- Explore upcoming sections: Internet history, browsers, HTML, CSS, JavaScript.

---