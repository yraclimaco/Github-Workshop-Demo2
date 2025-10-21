# 🧠 Git Hands-On: Clone, Merge, and Resolve Merge Conflicts

This tutorial walks you through simulating a **merge conflict** and resolving it manually.

## Section 1: Intro

These steps are to be done by **One** Person in your group. The other person will have things to do in the future don't worry! Please be sure to pay attention though.

### 🚀 Step 1. Fork this Repository

1. You can fork this repository by clicking the fork icon at the top. This will copy the repository into your Github account.

### 💻 Step 2. Clone Your Repository Locally

1. Expand the code button, select HTTPS, and copy the url.
2. Open your terminal (or Git Bash), then run:
```bash
git clone <url>
cd Github-Workshop-Demo2
```

### Step 3.📝 Create a file

1. Create a text file called adventure.txt using the `touch` command
2. Add and commit your file

```bash
git add .
git commit -m "Add adventure.txt"
git push
```

## Section 2: Branching, Merging and Merge Conflicts
### Step 1: Add as a collaborator!
Person 1, add person 2 as a collaborator on your new github repo!

### Step 2: Person 2, Clone the same repository

Follow the steps in section 1.2 to clone the same repository to your local working environment.

### Step 3: (Person 1&2) Create a new Branch

Create your own branches **with different names** and switch to it. The `-b` flag is a shortcut from doing `git branch [branch_name]` first.

```bash
git checkout -b [branch_name]
```

### Step 4: Edits!

On your local adventure.txt files, write these edits to them

- Person 1:
  - `The hero finds a magical sword. `
- Person 2:
  - `The Hero swings and misses. `

Save, then:

```bash
git add story.txt
git commit -m "updates!"
```

push your new changes

```bash
git push
```

### Step 5: Pull Request

Person 1 ones a pull request, adds a short description, and adds Person 2 as a reviewer.

Person 2 goes to Changed Files, reviews the changes and merge the pull request. You should have no conflicts at this point.

### Step 6: Merge and conflicts

Person 2 goes back to the main branch and pull the new changes

```bash
git checkout main
git pull
```

Person 2 tries to merge their branch into main.

```bash
git merge [branch_name]
```

You should see, and on VSCode, adventures.txt will open with the conflicts

```bash
Auto-merging adventure.txt
CONFLICT (content): Merge conflict in story.txt
Automatic merge failed; fix conflicts and then commit the result.
```

## Section 3: Resolving conflicts!

### Step 1: Resolve the conflict

Manually edit it to something like

```bash
The Hero finds a magical sword.
The Hero swings and misses
```

then mark it resolved and commit confirm merge on VScode.

```bash
git add adventure.txt
git commit -m "Resolve merge conflict"
```

push your updated main branch

```bash
git push
```

### Step 5: Clean up

If you’re done with the exercise, you can delete your branches:

```bash
git branch -d [branch_name]
git push origin --delete [branch_name]
```
