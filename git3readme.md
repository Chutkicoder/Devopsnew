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
b. Demonstrate branching and pull requests
Step 1: Create a Feature Branch
git checkout -b feature/greet-user
Step 2: Add New Code
Edit app.py:
name = input(&quot;Enter your name: &quot;)
print(f&quot;Hello, {name}!&quot;)

Then in Powershell:
git add app.py
git commit -m &quot;Add user greeting feature&quot;
git push origin feature/greet-user
Step 3: Create a Pull Request
1. Go to your repo on GitHub
2. You’ll see a prompt: “Compare &amp; pull request”
3. Click it → Add a description → Click “Create pull request”
4. Review and click “Merge pull request”
5. Confirm merge and delete branch (optional)

c. Simulate a conflict and resolve it
Step 1: Create Two Feature Branches from Main
git checkout main
git checkout -b feature/conflict-A
Change app.py:
print(&quot;This is branch A&quot;)
Then:
git add app.py
git commit -m &quot;Change message in branch A&quot;
git push origin feature/conflict-A
Optional:
Now create another conflicting branch:
git checkout main
git checkout -b feature/conflict-B
Edit the same line in app.py:
print(&quot;This is branch B&quot;)
Then:
git add app.py

git commit -m &quot;Change message in branch B&quot;
git push origin feature/conflict-B
OpOptional Close_____________

Step 2: Merge One Branch First (e.g., conflict-A)
 On GitHub → Create PR from feature/conflict-A → Merge into main
Step 3: Create PR from conflict-B
 On GitHub → Create PR from feature/conflict-B
 GitHub will detect a conflict
 Click “Resolve conflict”
 Manually fix the conflict. Example:
&lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
print(&quot;This is branch A&quot;)
=======
print(&quot;This is branch B&quot;)
&gt;&gt;&gt;&gt;&gt;&gt;&gt; feature/conflict-B
Edit it to:
print(&quot;This is the resolved version&quot;)
Click “Mark as resolved” → Commit → Merge the pull request
