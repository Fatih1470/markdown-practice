# markdown-practice
# How I Keep a File Out of GitHub

Sometimes I want to keep a file on my computer without uploading it to GitHub. Here is how I can do that with Git.

## The Files I Need

- `.gitignore` is where I write the names of files I want Git to ignore.
- `cachefile` is an empty file I use to test my rule.

## How I Test the Rule

1. Open the terminal in the project folder.
2. Write `cachefile` on a new line in `.gitignore`.
3. Create the empty file.
4. Ask Git to show the ignored files.

### The Commands I Use

```bash
echo cachefile >> .gitignore
touch cachefile
git status --short --ignored
```

### How I Read the Result

Git shows **two exclamation marks** next to an ignored file.

*The file is still in my project folder.*

***I can share the rule on GitHub and keep the test file on my computer.***

| File | What happens to it? |
| --- | --- |
| `.gitignore` | I commit this file and push it to GitHub. |
| `cachefile` | Git ignores it when I run `git add .`. |
