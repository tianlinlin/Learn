# git method to Load remote repository URL

To load repository we can use git method
```sh
git remote add origin <你的远程仓库URL>
```

# git method to Commit a single file to the repository
    the first step is Adding specified files to the staging area(缓存区)
```sh
git add 'filename'
```
**File names need to be presented as relative paths**
    then Commit the file (with a description)
```sh
git commit -m 'description'
```
    last Push to remote repository
```sh
git push origin main
```
Here, 'main' is the branch of the remote repository you want to import.
If you want to import a file into __a specific folder__ of a remote repository, simply ensure that the folder containing the file has **the same name** as the fold in repository, and then provide **the relative path** when running 'add'.

# Clear the staging area
```sh
git reset
git reset -- <文件路径>
```

# Delete a file and commit (removes both locally and remotely)
```sh
git rm <文件路径>          # 删除工作区和暂存区的文件
git commit -m "删除文件"
git push origin <分支名>
```
# Remove from the Git repository only, while keeping the working copy (local files not deleted)
```sh
git rm --cached <文件路径>
git commit -m "停止追踪文件"
git push
```
# Delete a directory(folder)