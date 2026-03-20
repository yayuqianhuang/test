# test

git init
在当前目录初始化一个新的 Git 仓库，创建一个名为 .git 的子目录，其中包含所有必要的版本控制元数据。如果目录非空，现有文件不会被自动跟踪，需要后续手动添加。

git checkout -b dev origin/dev
创建并切换到名为 dev 的新本地分支，同时将这个新分支设置为跟踪（关联）远程仓库（通常名为 origin）中的 dev 分支。这常用于在本地开始基于远程某个分支进行工作。

git pull
从当前分支所跟踪的远程分支（默认为 origin）获取最新的提交，并自动合并到当前本地分支。它相当于依次执行 git fetch 和 git merge 两个命令。

git branch -a
列出所有分支，包括本地分支和远程跟踪分支。远程分支通常会以 remotes/ 开头（例如 remotes/origin/main），方便查看仓库的全貌。

git branch -d <branch_name>
安全地删除指定的本地分支。Git 会检查该分支的更改是否已经完全合并到当前分支，如果未合并则会阻止删除，防止工作丢失。

git checkout -b feature
基于当前所在分支，创建并切换到一个名为 feature 的新本地分支。这个新分支最初没有关联任何远程分支，通常用于开发新功能或修复问题。

git add . 与 git commit -m “提交信息”
这是两个命令的组合。git add . 将当前目录下所有新的或修改过的文件添加到暂存区（Staging Area），准备提交。git commit -m “...” 则将暂存区的内容创建一个永久的快照（提交）保存到本地仓库，并附上说明信息。

git merge feature
将指定分支（这里是 feature）上的所有修改合并到当前所在的分支。如果两个分支对同一文件的修改有冲突，Git 会提示需要手动解决。

git branch -d feature
在 feature 分支的功能开发完成并成功合并到主分支（如 main）后，使用此命令删除该本地分支，以保持工作区的整洁。

