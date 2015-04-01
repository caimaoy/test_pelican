Title: 使用Pelican在Github上建立个人博客
Date: 2015-04-01 09:51
Modified: 2015-04-01 09:51
Category: blog
Tags: python, github, pelican
Slug: build-blog-on-github-with-pelican
Author: caimaoy


#相关连接
- [基础篇](http://www.xycoding.com/articles/2013/11/21/blog-create)
- [进阶篇](http://www.xycoding.com/articles/2013/11/22/blog-advance)  
- 有以上的连接我就不再赘述了，讲讲一些其他的坑

#基础知识
- python
- git
- github

#配置文件
| 这个应该是说得比较多的一部分了，因为使用windows(我也不想用！！！)不得不改动一下
    配置文件  

##重点修改如下

    git_test: publish
        git push origin $(GITHUB_PAGES_BRANCH)
        ghp-import -b $(GITHUB_SOURCE_BRANCH) $(BASEDIR)
        git push origin $(GITHUB_SOURCE_BRANCH)

其中git的部分你懂就应该懂，说一下ghp-import，可以使用pip安装但是如果是你windows
用户请考文章http://docs.getpelican.com/en/latest/tips.html#publishing-to-github
如果你无法用下面的方法安装，请下载后python setup.py install

```
ghp-import on Windows

Until ghp-import Pull Request #25 is accepted,you will need to install a custom build of ghp-import:
pip install https://github.com/chevah/ghp-import/archive/win-support.zip

```
