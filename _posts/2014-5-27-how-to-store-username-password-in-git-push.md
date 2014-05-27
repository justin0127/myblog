---
layout: post
title: git push避免用户名密码方法
---

##方法一
	
####创建文件存储GIT用户名密码

在%home%目录中，创建.git-credentials文件并在其中写入GIT的用户名和密码

cd ~
touch .git-credentials

vim .git-credentials

https://{username}:{password}@github.com

{: .prettyprint .lang-shell}
