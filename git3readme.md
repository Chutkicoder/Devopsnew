git --version
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
create repo
git clone https://github.com/username/Forcheckingpurpose.git
cd Forcheckingpurpose
git add .
git commit -m "Add files from new PC"
if any error:
git commit -m "Add files from new PC"
git remote add origin https://github.com/username/Forcheckingpurpose.git
git branch -M main
git push -u origin main
git remote -v //{ftch}{push}
git add .
C:\Forcheckingpurpose>git commit -m "Initial commit"
git push -u origin main
//branch 'main' set up to track 'origin/main'.
//Everything up-to-date
----docsteppart------
b. Demonstrate Branching and Pull Requests
Step 1: Create a Feature Branch
git checkout -b feature/greet-user


This creates a new branch called feature/greet-user and switches to it.

Step 2: Add New Code

Edit app.py:

name = input("Enter your name: ")
print(f"Hello, {name}!")


Then in PowerShell:

git add app.py
git commit -m "Add user greeting feature"
git push origin feature/greet-user

Step 3: Create a Pull Request on GitHub

Go to your repo → You’ll see: “Compare & pull request”

Click it → Add a description → Click “Create pull request”

Review → Click “Merge pull request”

Confirm merge → Optionally delete the feature branch

c. Simulate a Conflict and Resolve It
Step 1: Create Two Conflicting Feature Branches

Branch A:

git checkout main
git checkout -b feature/conflict-A


Edit app.py:

print("This is branch A")

git add app.py
git commit -m "Change message in branch A"
git push origin feature/conflict-A


Branch B:

git checkout main
git checkout -b feature/conflict-B


Edit the same line in app.py:

print("This is branch B")

git add app.py
git commit -m "Change message in branch B"
git push origin feature/conflict-B

Step 2: Merge One Branch First (e.g., conflict-A)

On GitHub → Create PR from feature/conflict-A → Merge into main

Step 3: Create PR from conflict-B

On GitHub → Create PR from feature/conflict-B

GitHub detects a conflict → Click “Resolve conflict”

Edit the file to resolve the conflict:

<<<<<<< HEAD
print("This is branch A")
=======
print("This is branch B")
>>>>>>> feature/conflict-B


Edit to final resolved version:

print("This is the resolved version")


Click Mark as resolved → Commit → Merge the pull request
