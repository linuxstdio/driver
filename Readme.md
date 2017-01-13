驱动学习版本记录：


git 规范
1.创建分支
	git checkout master
	git pull
	git checkout -b myfeature

2.提交分支commit
	git add -all
	git status
	git commit --verbose

3.撰写提交信息
	第一行不超过50个字
	第二行：罗列出改动的原因，主要变动，以及需要注意的问题。

4.与主干同步
	git fetch origin
	git rebase origin/master

5.合并commit
	git rebase -i origin/master
	pick:正常选中
	reword：选中，并且修改提交信息
	edit：选中，rebase时会暂停，允许你修改这个commit
	squash:选中，会将当前commit与上一个commit合并。
	fixup:与squash相同，但不会保持当前commit的提交信息。
	exec:执行其他shell命令。
	
	squash/fixup命令，还可以当作命令行参数使用，自动合并commit.

6.推动到远程仓库

