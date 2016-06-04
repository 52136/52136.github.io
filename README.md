# welcome to 52136.github.io
/*
*this is a blog example
*/
#利用github搭建部署个人博客实践
##1、注册github账号（52136）
##2、创建仓库repository（52136.github.io）。备注必须和账号名相同
##3、依次安装以下两个软件
  <p> a)Node.js</p>
  <p> b)Github for windows</p>
##4、在windows中打开CMD，然后依次执行如下命令：
  <p>a)ssh -T git@github.com\<br></p>
  <p>b)安装hexo：（系统会自动添加目录到PATH环境变量）</p>
    <p>i.cd  /     设置安装目录\<br></p>
    <p>ii.npm install hexo-cli -g\<br></p>
    <p>iii.cd Hexo		（进入Hexo目录）</p>
    <p>iv.npm install</p>
    <p>v.hexo generate </p>
    <p>vi.hexo server</p>
<p>备注：需设置环境变量：http://www.cnblogs.com/SCOOL/p/4054045.html</p>
##5、此时打开浏览器，在浏览器地址栏输入 http://localhost:4000/ （默认端口为4000）, 便可以看到最原始的博客了。

#【将本地文件部署到github上】
##1、修改 Hexo 中的 _config.yml 文件
  <p>http://github.com/52136/52136.github.io.git</p>
##2、执行如下命令
  <p>a)hexo clean</p>
  <p>b)hexo generate</p>
  <p>c)hexo deploy</p>
<p>错误处理方法：</p>
  <p>将deploy 的 type 改成 git，然后再在 Git Shell 中运行以下命令:</p>
  <p>npm install hexo-deployer-git --save</p>
<p>再重新来一遍：</p>
  <p>1)hexo clean</p>
  <p>2)hexo generate</p>
  <p>3)hexo deploy</p>
  
<p>解决办法：</p>
<p>执行这两条命令即可解决</p>
<p>$git config --global user.email {emailaddress}</>
<p>$git config --global user.name {name}</p>
##3、成功界面
<p>恭喜，到这一步，个人博客就已经部署到 GitHub 上了，你可以到你的GitHub仓库查看是否已经更新。此时,通过 your_user_name.github.io（即你那个仓库的名称，形如：”你的 GitHub 用户名”.github.io）,就可以看到你的个人博客了。
