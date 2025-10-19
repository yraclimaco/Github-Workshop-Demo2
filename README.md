# 🧠 Git Hands-On: Clone, Merge, and Resolve Merge Conflicts

This tutorial walks you through simulating a **merge conflict** and resolving it manually.

## Section 1: Intro

These steps are to be done by **One** Person in your group. The other person will have things to do in the future don't worry! Please be sure to pay attention though.

### 🚀 Step 1. Create a GitHub Repository

1. Go to [GitHub](https://github.com) and click **New Repository**.
2. Name it something like: DS3-Demo2
3. Make sure repository access is set to **Public**

### 💻 Step 2. Clone Your Repository Locally

Open your terminal (or Git Bash), then run:

```bash
git clone https://github.com/<your-username>/DS3-Demo2.git
cd git-merge-practice
```

### 📝 Step 3. Add This README

1. Download this README file and place it into the folder you just created on your laptop
2. Add and commit your file

```bash
git add .
git commit -m "Add README"
git push
```

### Step 4.📝 Another file

1. Create a text file and name it adventure.txt
2. Add and commit your file

```bash
git add .
git commit -m "Add adventure.txt"
git push
```

## Section 2: Branching, Merging and Merge Conflicts

### Step 1: Person 2, Clone the same repository

Follow the steps in section 1.2 to clone the same repository to your local working environment.

### Step 2: (Person 1&2) Create a new Branch

Create your own branches and switch to it

```bash
git checkout -b [Your_Name]
```

### Step 2: Edits!

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
git push -u origin [Your_Name]
```

### Step 3: Merge and conflicts

Go back to the main branch

```bash
git checkout main
```

try to merge both of your changes to main, Person 2 followed by Person 1

```bash
git merge [Your_Name]

```

you should see, and on VSCode, adventures.txt will open with the conflicts

```bash
Auto-merging story.txt
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

then mark it resolved and commit on main:

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
git branch -d [Your_Name]
git push origin --delete [Your_Name]
```
