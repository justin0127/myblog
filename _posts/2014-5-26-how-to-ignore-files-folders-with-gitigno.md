---
layout: post
title: 2014-5-27-工作日志
---

##2014-5-26-how-to-ignore-files-folders-with-gitignore

git提交的时候常常会把一些不需要提交的文件也提交上去，如配置文件、class编译文件、release文件等，因此需要控制特定的文件或特定目录不需要Git管理。

在代码目录下建立起.gitignore文件

	vim .gitignore 
{: .prettyprint .lang-shell}

文件内容如下:

	#过滤数据库文件、sln解决方案文件、配置文件
	*.mdb
	*.ldb
	*.sln
	*.config
{: .prettyprint .lang-shell}


	#过滤文件夹Debug,Release,obj
	Debug/
	Release/
	obj/
{: .prettyprint .lang-shell}
	
如果在建立.gitignore 之前就提交过，则需要把index.cache和history.cache都删掉，重新commit

	git rm -f myfile/history.cache
	git rm -f myfile/index.cache
{: .prettyprint .lang-shell}
