---
layout: post
title: git push避免重复输入用户名密码方法
---

##1. 方法一 存储在GIT配置文件中
	
####1.1 创建文件存储GIT用户名密码

在%home%目录中，创建.git-credentials文件并在其中写入GIT的用户名和密码

	cd ~
	touch .git-credentials
	vim .git-credentials
	https://{username}:{password}@github.com
{: .prettyprint .lang-shell}

####1.2 添加git config 内容

进入git bash 终端，输入如下内容

	git config --global credential.helper store
{: .prettyprint .lang-shell}

执行完后查看%HOME%目录下的.gitconfig文件，会多了一项：

	[credential]
    helper = store
{: .prettyprint .lang-shell}

重新开启git bash会发现git push时不用再输入用户名和密码

##2. 方法二 window 环境变量

