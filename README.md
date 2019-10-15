# 蓝云研究院技术认证——PowerShell

Blue Cloud Certified - PowerShell

# 学习材料包括

  文字稿  
  PPT  
  视频

# 协作前的准备工作
  
  1、注册Github个人账号，将帐号发给Project Owner  
  2、注册Teambition帐号，将帐号发给Project Owner
  3、在本地安装Git和VS Code  
  4、将BCC-PS仓库克隆至自己的本地，命令如下：  
  ```powershell
  cd $home\documents  #切换到希望本地仓库所存放的路径
  git clone https://github.com/vFrankPZhang/BCC-PS.git BBC-PS
  ```

# 协作步骤

  1、依据确定好的章节，建立每章的Branch  
  2、每章的owner建立基于章节的Branch，建立以自己名字为前缀的Branch，在Teambition中，将任务状态移至“进行中”  
  3、每章的owner完成内容编写后，pull request回章节的Branch上，并进行merage，在Teambition中，将任务移至“校对进行中”开始校对工作  
  4、其他人为章节的Branch进行校对，完成后pull request回内容的Branch，直至校对完成后，章节Owner在Teambition中，将任务移至“内容已完成”  


# 协作示例

假如，你现在是Part.Test章节的Owner

  1、打开PowerShell，进入仓库“BBC-PS”所在的路径：
  ```powershell
  PS > cd $home\document\BBC-PS
  ```
  2、执行git pull，将本地的仓库更新至与远端一致
  ```powershell
  PS > git pull
  ```
  3、




以Wind来完成readme内容的创作，其他人校对为例：

  1、Wind在自己的本地，将Git分支切换到readme分支  
  ```powershell
  PS >git checkout readme
  ```  
  2、基于readme分支创建自己名字的分支
  ```powershell
  PS >git checkout -b 'wind/readme'
  ```
  3、完成文档的创作  
  4、将自己的分支push回Frank的Github
  ```powershell
  PS >git push origin wind/readme
  ```
  5、提交Pull Request到readme分支  
  1）登录自己的Github帐号  
  2）用浏览器进入：https://github.com/vFrankPZhang/BCC-PS  
  3）点击“Pull requests”标签  
  ![](images/readme.pullrequest.1.png)
  4）点击“New pull request”按钮  
  ![](images/readme.pullrequest.2.png)
  5）选择清楚，pull request的方向，点击“Create new pull request”按钮，完成Pull request  
  ![](images/readme.pullrequest.3.png)
  ![](images/readme.pullrequest.4.png)
  6）Wind直接将wind/readme分支Merge到readme分支里
  ![](images/readme.pullrequest.5.png)
  6、建坤重复上面的步骤，校对Wind pull request之后的branch，pull request，然后由Wind改进自己的内容，确定是否Merge或者修改自己的内容。

# 文字稿

## 完成文字稿的具体步骤

  1、章的划分、排序，每章目标的说明，及不同章的顺序的逻辑  
  2、根据确定的章，确定节的内容纲要  
  3、根据节的内容纲要确定内容的标准及要求，如：需要有知识讲解、截图、练习  
  4、分工开始具体写  
  5、完成文字稿工作

> ### 需要的背景知识
>
> PowerShell  
> Markdown  
> Git  
