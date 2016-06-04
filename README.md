# 52136.github.io
/*
this is a blog example
*/

利用github搭建部署个人博客实践
1、注册github账号（52136）
2、创建仓库repository（52136.github.io）。备注必须和账号名相同
3、依次安装以下两个软件
  a)Node.js
  b)Github for windows
4、在windows中打开CMD，然后依次执行如下命令：
  a)ssh -T git@github.com
  b)安装hexo：（系统会自动添加目录到PATH环境变量）
    i.cd  /     设置安装目录
    ii.npm install hexo-cli -g
    iii.cd Hexo		（进入Hexo目录）
    iv.npm install
    v.hexo generate 
    vi.hexo server
备注：需设置环境变量：http://www.cnblogs.com/SCOOL/p/4054045.html
5、此时打开浏览器，在浏览器地址栏输入 http://localhost:4000/ （默认端口为4000）, 便可以看到最原始的博客了。


【将本地文件部署到github上】
1、修改 Hexo 中的 _config.yml 文件
  http://github.com/52136/52136.github.io.git
2、执行如下命令
  a)hexo clean
  b)hexo generate
  c)hexo deploy
错误处理方法：
  将deploy 的 type 改成 git，然后再在 Git Shell 中运行以下命令:
  npm install hexo-deployer-git --save
再重新来一遍：
  1)hexo clean
  2)hexo generate
  3)hexo deploy
  
解决办法：
执行这两条命令即可解决
$git config --global user.email {emailaddress}
$git config --global user.name {name}
3、成功界面
恭喜，到这一步，个人博客就已经部署到 GitHub 上了，你可以到你的GitHub仓库查看是否已经更新。此时,通过 your_user_name.github.io（即你那个仓库的名称，形如：”你的 GitHub 用户名”.github.io）,就可以看到你的个人博客了。
