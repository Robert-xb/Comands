### Git常用命令汇总

#### 第一次使用

	- 初始配置
	$git config --global user.name 'name'
	$git config --global user.email 'xxx@xx.com'

	- 初始化
	$git init

	- 关联GitHub和gitee
	$ssh-keygen -t rsa -C 'xxx@xx.com'
	$cd ~/.ssh
	$ls
	$cat id_rsa.pub
	复制秘钥添加到GitHub和gitee上的settings里的ssh处
	$git remote add github git@github.com:xcalan/learn_git.git
	$git remote add gitee git@gitee.com:xcalan/learn_git.git

	- 第一次建立本地库和github的联系
	$git pull github master

	- 提交到暂存区和本地仓库
	$git add filename
	$git commit -m 'description'

	- 第一次push到github
	$git push github master

	- 第一次建立本地库和gitee的联系
	$git pull gitee master
	报错出现conflict，修改冲突，手动合并之后
	$git add '修改好的文件名'
	$git commit -m 'description'

	- 第一次push到gitee
	$git push gitee master

#### 本地库和github和gitee关联好之后的更新合并
	
	- 只有本地更新
	$git add filename
	$git commit -m 'description'
	$git push github master
	$git push gitee master

	- 本地库和远程库都有更新的情况下的合并，以github有更新为例
	$git fetch github master
	$git merge github/master
	提示冲突，手动修改合并要保留的内容后
	$git add filename
	$git commit -m 'description'
	$git push github master

	- 本地库、github和gitee三个地方同时做了修改后的合并，先将两个库之间的更新进行合并再与第三个库进行合并。
	$git fetch github master
	$git merge github/master
	报错出现conflict，手动修改合并保留之后
	$git add filename
	$git commit -m 'description'
	$git push github master
	$git fetch gitee master
	$git merge gittee/master
	报错出现conflict，手动修改合并保留之后
	$git add filename
	$git commit -m 'description'
	$git push gitee master
	(完成三个库的合并）


#### 常规操作
	
	$git branch 分支名字	//建立分支

	
	$git checkout 分支名字	//切换分支
	$git switch 分支名字

	$git branch	//查看分支，必须要建立跟远程库的联系以后才可以查看到
			
	$git remote -v	//查看关联的远程库的信息

	$git status	//查看当前库的状态
	$git diff	//查看当前相对上一次提交修改的内容

	$git merge 分支名字	//指定分支合并到当前分支上
	$git branch -d 分支名字 //删除分支

	$git log --graph	//查看分支合并图

	$git tag v1.0		//给当前分支打新的标签
	$git tag 		//查看所有标签
	
	$git config --global color.ui true	//改变git颜色








