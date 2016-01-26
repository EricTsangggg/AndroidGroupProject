mac下使用git的基本方法</br>
（window下的命令应该大致一样，有不清楚处可以自己上网GOOGLE摸索下）</br>
（如有错误请纠正我）</br>

1.通过Android Studio的Preference的VCS中的git安装git</br>
2.mac中打开 Terminal</br>
3.尝试以下命令</br>
</br>
cd  /xxx/xxx..../Project      //进入到你的代码所在的project目录下 (使用cd ..   可以返回上一级)</br>
ls  -a      ﻿    ﻿  //查看目录下的文件</br>
</br>
git init               //进入项目所在目录进行git初始化</br>
git status            //查看git状态</br>
</br>
git add .                //将未标记版本内容加入git  (注意add后有一个小点不能少）</br>
git branch                //查看git的branch</br>
git branch xxx             //添加branch，xxx为branch名字,github上默认的是master</br>

git remote add xxx url                //添加远程github的URL (例如https://github.com/EE5415/AndroidGroupProject.git) ，xxx为自己定义的repository名字</br>
git remote rm xxx                 //删除远程repository</br>
git fetch                                 //从远程获取最新版本到本地，不会merge</br>
git commit -m "commit notation"       //将changes提交到本地repository，commit notation为自定义的标签，随便写</br>
git pull origin master        //从远程获取最新版本并merge到本地(此处origin为repository名字，master为branch名字</br>
git push origin master       //将本地repository最新的changes提交到远程github的repository           </br> 
</br>
git branch tmp                        //以下4个命令为一组，作用是切换branch，tmp是临时branch</br>
git checkout master</br>
git merge tmp</br>
git branch -d tmp    (-D)            //删除tmp</br>


正常来说一个未加入本地git的项目的代码的上传到github的流程是：</br>
-->git init</br>
-->git add .</br>
-->git commit -m "whatever"</br>
-->git branch test</br>
-->git checkout test</br>
-->git merge test</br>
-->git remote add android https://github.com/EE5415/AndroidGroupProject.git</br>
-->git push android test</br>

=========================================================================================================================
=========================================================================================================================

//如果URL是SSH的，就需要创建SSH的密钥,https则不需要</br>
CREATE SSH:                                </br>
1. cd ~/.ssh</br>
2.ls</br>
3.if there are id_rsa.pub pr id_dsa.pub</br>
4.if not</br>
5.ssh-keygen -t rsa -C "email address"</br>
6.add the ssh key to github account</br>
7.GITHUB.com----->Settings----->title&key----->bundle</br>
8.Xcode----->Source Control------>remotes---->add remotes--->push</br>
