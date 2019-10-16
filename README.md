# 蓝云研究院技术认证——PowerShell

Blue Cloud Certified - PowerShell

# 我们要准备的学习材料包括

  文字稿  
  PPT  
  视频

# 需要的背景知识

PowerShell  
Markdown  
Git  

# 协作前的准备工作
  
  1、注册Github个人账号，将帐号发给Project Owner  
  2、注册Teambition帐号，将帐号发给Project Owner
  3、在本地安装Git和VS Code  
  4、将BCC-PS仓库克隆至自己的本地，命令如下：  
  ```powershell
  cd $home\documents  #切换到希望本地仓库所存放的路径
  git clone https://github.com/vFrankPZhang/BCC-PS.git BBC-PS
  ```

# 总体协作步骤

  1、（Owner）依据确定好的章节，建立每章的章节Branch。例如：“PartA”。  
  2、（章节owner）建立以自己名字为前缀的个人章节Branch，并进行编辑。例如：“Wind/PartA”。并在Teambition中，将任务状态移至“进行中”。  
  3、（章节owner）完成内容编写后，进行“pull request”操作，并 **<mark style="color: Green">直接进行merage操作</mark>**。在Teambition中，将任务移至“校对进行中”开始校对工作。  
  4、（参与者）其他人为章节进行校对编辑。同样创建个人Branch，例如：“JK/PartA”。完成校对编辑后，将个人Branch向章节Branch进行“pull request”请求。**<mark style="color: Red">但不进行merge</mark>**。  
  5、（章节Owner）在校对“pull request”中进行检查。并与参与者沟通修改内容。完成后进行merge操作。章节Owner在Teambition中，将任务移至“内容已完成”。  


# 参与者协作示例

假如，你现在是Part.Test章节的Owner

2.0 将BCC-PS仓库克隆至自己的本地，命令如下：  
  ```powershell
  PS> git clone https://github.com/vFrankPZhang/BCC-PS.git BBC-PS  
  ```

2.1 打开PowerShell，进入仓库“BBC-PS”所在的路径：
```powershell
PS> cd $home\document\BBC-PS
```

2.2 执行git pull，将本地的仓库更新至与远端一致
```powershell
PS> git pull
```
2.3 查看仓库中有哪些branch
```powershell
PS> C:\Users\vFrank\Documents\BCC-PS> git branch -a

master
remotes/origin/HEAD -> origin/master
remotes/origin/master
remotes/origin/part.test
```
2.4 切换到part.test分支
```powershell
PS> C:\Users\vFrank\Documents\BCC-PS> git checkout part.test
Switched to branch 'part.test'
```
2.5 创建以自己名字为前缀的part.test分支
```powershell
PS> C:\Users\vFrank\Documents\BCC-PS> git checkout -b you/part.test
Switched to a new branch 'you/part.test'
```
2.6 在Teambition中将任务从“待处理”移至“编写进行中”

![teambition](images/readme.teambition.1.png)

3.1 编写内容  

比如你在you/part.test中，新建一个test.md的文件，内容为test,并保存文件

3.2 将文件提交给git来管理
```powershell
git add .
git commit -m 'add test.md'
```
3.3 将you/part.test分支推送到Frank's的github上
```powershell
git push
```
这时，Frank的github上就会有了you/part.test这个分支

![pull request](images/readme.pullrequest.1.png)

3.4 将你的分支you/part.test pull request 给part.test

![pull request](images/readme.pullrequest.2.png)

注意，选择好pull request的方向，在这里，你需要把you/part.test pull request 给part.test，因为这样，按我们定好的流程，别人就可以去基于你更新后的part.test去进行校对工作。

![pull request](images/readme.pullrequest.3.png)

![pull request](images/readme.pullrequest.4.png)

3.5 Merge这个Pull request <mark>(只有章节owner才可以进行merge操作)</mark>

![pull request](images/readme.pullrequest.5.png)

3.6 在Teambition中，将任务移至“校对进行中”

![teambition](images/readme.teambition.2.png)

至此，文章的Owner就完成了自己部分的内容的创建。  

4.1 对于校对的人，跟上面的步骤是一样的，只是，不要做3.5这一步，由章节的Owner来决定是否要Merge。  
4.2 当所有需要校对的人，完成校对之后，由章节的owner在Teambition中将任务移至“校对已完成”  
4.3 最后由Project Owner确认内容，在Teambition中将任务移至“内容已完成”  

# 文字稿

## 完成文字稿的具体步骤

  1、章的划分、排序，每章目标的说明，及不同章的顺序的逻辑  
  2、根据确定的章，确定节的内容纲要  
  3、根据节的内容纲要确定内容的标准及要求，如：需要有知识讲解、截图、练习  
  4、分工开始具体写  
  5、完成文字稿工作
