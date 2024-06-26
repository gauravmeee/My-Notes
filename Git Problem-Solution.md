# Create New Repository
```bash
echo "# My-Notes" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/gauravmeee/My-Notes.git
git push -u origin master
```
# Push existing repository
```bash
git remote add origin https://github.com/gauravmeee/My-Notes.git
git branch -M master
git push -u origin master
```


# 1. To ignore node_modules (prevent from uploading on github)
1.  create a `.gitignore` file in project's root directory 
```bash
touch .gitignore
```
 manually specify this line in the file
   ```.gitignore
   node_modules/
   ```

**or**
Create and update the .gitignore file through command line

```bash
echo "node_modules/" >> .gitignore
```

2.  Save and commit

  ```bash
  git add .gitignore #Stage the .gitignore file:
  git commit -m "Add .gitignore to exclude node_modules" #Commit the changes
  ```
3. Check `node_modules` not included in the list of files to be committed
   ```bash
    git status
   ```
# 2. Upload Project to Github

1. Add the remote repository (if not already added):
   ```bash
   git remote add origin https://github.com/gauravmeee/REST-API- NERVESPARKS-Assignment.git
   ```
2. Push to the `master` branch
   ```bash
   git push origin master
   ```
# 3. Remote origin already exists

1. Update the Exisiting Remote 
   ```bash
   git remote set-url origin https://github.com/gauravmeee/REST-API-NERVESPARKS-Assignment.git

   git push origin master #push 
   
   ```
   **or**

2. Use a Different Remote Name
   ```bash
   git remote add upstream https://github.com/gauravmeee/REST-API-NERVESPARKS-Assignment.git
   
   git push upstream master #push to this new remote
   ```

3. Verify the Remote Configuration
   ```bash
   git remote -v #list of all configured remotes and their URLs.
   ```
# 4 failed to push some refs to ... Updates were rejected because the remote contains work that you do not
hint: have locally....

1. Fetch the remote changes
   ```bash
   git fetch origin #update only the local repository
   ```
2. Merge the remote changes into your local branch
   ```bash
   git merge origin/master
   ```
3.  Handling Merge Conflicts
Open the conflicting files in your text editor and look for the conflict markers (<<<<<<<, =======, >>>>>>>). Resolve the conflicts by choosing the appropriate changes.

4. ```bash
   git add path/to/resolved/file #stage the resolved files
   git commit #commit the merge
   git push origin master #git push origin master
   ```
# 5 failed to push some refs to ...Updates were rejected because the tip of your current branch is behind

1. Pull the latest changes from the remote repository
   ```bash
   git pull origin master #updates both the local repository and the working directory.
   ```
2. {*Resolve any Merge Conflict by Point `#4.3`}

3. {*Repeat point `#4.4`}

# 6 fatal: refusing to merge unrelated histories

occurs when Git detects that the histories of the local and remote branches do not share a common base commit. 

1. Force the merge: Pull the latest Changes
   ```bash
   git pull origin master --allow-unrelated-histories
   ```
2. {Resolve any Merge Conflict by Point `#4.3`}
3. {Repeat point `#4.4`}
   
