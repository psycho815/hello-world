- [安装使用](#part1)
- [创建一个repository流程](#part2)
- [实践操作命令](#part3)



# git

- **$ git init** 新建repository文件后执行 
- **$ git remote add origin git@github.com:psycho815/gulp-workflow.git** 添加远程地址
- **$ git pull** 线上更改时先执行 
- **$ git add RADME** 或者  **$ git add .**  
- **$ git add -u**   add to index only files modified or deleted and not those created 
- **$git add -u [< path >]**  把< path >中所有tracked文件中被修改过或已删除文件的信息添加到索引库。它不会处理untracted的文件。
省略< path >表示.,即当前目录。
- **$git add -A: [< path >]** 表示把< path >中所有tracked文件中被修改过或已删除文件和所有untracted的文件信息添加到索引库。
省略< path >表示.,即当前目录。
- **$git add -i [< path >]** 命令查看< path >中被所有修改过或已删除文件但没有提交的文件，
并通过其revert子命令可以查看< path >中所有untracted的文件，同时进入一个子命令系统。
- **$ git commit -m 'first commit'**
- **$ git push origin master**

# <span id="part1">安装使用 </span>

**步骤一：**在github创建新的repository仓库例如：'hello-world'

步骤二：安装git客户端 

windows用户请下载 [http://msysgit.github.com/](http://msysgit.github.com/)
mac用户请下载 [http://code.google.com/p/tortoisegit/](http://code.google.com/p/tortoisegit/)
安装完成后，右键会多出一些菜单。如 Git Init Hear、Git Bash、Git Gui ， 说明安装成功。

注意：安装到在“Adjusting your PATH environment”选项中一步。选择第一个“Use Git Bash Only ”

**步骤三：**本地新建'hello-world'文件夹并右键'Git Bush Here'执行

    $ git init
(目录下生成一个.git文件则成功)

步骤四：在本地创建ssh key

    $ ssh-keygen -t rsa -C "your_email@youremail.com"
 按回车不设密码

 进入C:\Users\生\.ssh 打开id_rsa.pub 复制里面的key 
 到github.com网站 "settings"→"SSH and GPG keys"→"New SSH key"

验证是否成功

    $ ssh -T git@github.com
输出以下则成功
Warning: Permanently added the RSA host key for IP address '192.30.252.129' tohe list of known hosts.
Hi psycho815! You've successfully authenticated, but GitHub does not provide sll access.

设置username和email

    $ git config --global user.name "your name"
    $ git config --global user.email "your_email@youremail.com"


   -------------------（克隆github上的仓库到本地）在本地github文件目录执行 $git init 
   ------------------- $ git clole git@github.com:psycho815/hello-world.git

**步骤五：**添加远程地址

    $ git remote add origin git@github.com:psycho815/gulp-workflow.git
地址在github.com上copy

**步骤六：**执行add commit push等命令

***

# <span id="part2">创建一个repository流程</span>

1. 在github上新建 “New repository”，例如：articles
2. 本地目录新建articles，并右键'Git Bush Here'执行
3. 执行以下命令

'

        echo "# articles" >> README.md
        git init
        git add README.md
        git commit -m "first commit"
        git remote add origin git@github.com:psycho815/articles.git
        git push -u origin master

4. 执行

'

        $ git pull
        $ git add .
        $ git commit -m 'message'
        $ git push origin master

注意：线上更改时先执行 $ git pull


# <span id="part3">实践操作命令</span>
- $ git add -u film (单独提交某个文件夹或者文件/比如my-life下面的film修改了)
- $ git diff （显示修改的部分）