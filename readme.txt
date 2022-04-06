1.尼玛的，账号密码方式不给用了。2021-8-21开始要使用令牌方式，密码就是令牌
2.工作/git目录下有关于令牌的教程
3.你妈的，ssh也换新的密钥方式了  直接命令行ssh-keygen -t ed25519 -C "your_email@example.com" 生成新的私钥，公钥，再把新的私钥加载到ssh2->general
4.pull项目可能有问题，需要打开temp-git-configration-repository settings 选择不能pull的项目，open，添加：

[remote "origin"]
	url = https://gitee.com/gitee13192237903/demo-test.git
	fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
	remote = origin
	merge = refs/heads/master