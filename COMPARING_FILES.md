# How to Compare Files

A quick reference for comparing files — useful whether you're working with Git, the command line, or a text editor.

---

## Using Git

### Compare uncommitted changes to the last commit
```bash
git diff
```

### Compare a specific file
```bash
git diff path/to/file.txt
```

### Compare two commits
```bash
git diff <commit1> <commit2>
```

### Compare two branches
```bash
git diff main feature-branch
```

### Compare the staged (added) changes
```bash
git diff --staged
```

---

## Using the Command Line

### `diff` (Linux / macOS / Git Bash on Windows)
```bash
diff file1.txt file2.txt
```

Side-by-side view:
```bash
diff -y file1.txt file2.txt
```

### `fc` (Windows Command Prompt)
```cmd
fc file1.txt file2.txt
```

---

## Using a Visual Tool

Many editors and tools can compare files side-by-side:

| Tool | How to open a diff |
|---|---|
| **VS Code** | Right-click a file → *Select for Compare*, then right-click another → *Compare with Selected* |
| **GitHub** | Open a Pull Request — every changed file is shown with line-by-line differences |
| **WinMerge** (Windows) | File → Open, select both files |
| **Meld** (Linux) | `meld file1.txt file2.txt` |

---

## Reading a Diff

```
- this line was removed
+ this line was added
  this line is unchanged
```

Lines starting with `-` exist only in the **old** version.  
Lines starting with `+` exist only in the **new** version.

---

## Tips for Beginners

- `git diff` is your best friend when you want to see exactly what changed before committing.
- On GitHub, every Pull Request automatically shows a diff — no extra setup needed.
- VS Code's built-in diff viewer is great for comparing two local files without any extra tools.
