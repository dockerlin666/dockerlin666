# dockerlin666.github.io
dockerline blog

建立163邮箱 dockerlin@163.com
建立github账号和码云账号 dockerlin666

github建立仓库dockerlin666.github.io，注意只有选择这个名字才能直接访问dockerlin666.github.io，否则链接地址是dockerlin666.github.io/仓库名
选中项目，点击setting，往下拉到GitHub Pages，选择choose theme，随便选一个，提交文件，再选source为master，博客dockerlin666.github.io/就建好了

码云建立仓库dockerlin666，注意只有选择这个名字才能直接访问https://dockerlin666.gitee.io/，否则是https://dockerlin666.gitee.io/仓库名
选择项目，点击管理，选择基本配置，在项目远程地址(用于强制同步)框中填写https://github.com/dockerlin666/dockerlin666.github.io.git，保存后点击
最上面项目名边上的同步按钮。在服务里点击gitee page，选中开启，博客https://dockerlin666.gitee.io/建好了

建立ssh key

cd ~/.ssh
ssh-keygen -t rsa -C "dockerlin@163.com" -f dockerlin
vi dockerlin.pub
拷贝内容加入到github和gitee中ssh私钥中
vi config.php
  #dockerlin666-github
 host githubdocker
 user git
 hostname github.com
 port 22
 identityfile ~/.ssh/dockerlin
#dockerlin666-gitee
 host giteedocker
 user git
 hostname gitee.com
 port 22
 identityfile ~/.ssh/dockerlin
 
 测试
 ssh -T git@giteedocker
 Hi dockerlin666! You've successfully authenticated, but Gitee.com does not provide shell access.  
 ssh -T git@githubdocker
 Hi dockerlin666! You've successfully authenticated, but GitHub does not provide shell access.

