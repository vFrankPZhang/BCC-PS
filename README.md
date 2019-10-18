# 蓝云研究院技术认证——PowerShell

Blue Cloud Certified - PowerShell

## 我们要准备的学习材料包括

文字稿  
PPT  
视频

## 需要的背景知识

PowerShell  
Markdown  
Git  

## 协作前的准备工作
  
1.注册Github个人账号
2.将项目的仓库Fork到自己的Github中  

仓库地址：https://github.com/vFrankPZhang/BCC-PS.giBBC-PS  

通过浏览器进入到仓库，点击Fork，将该项目Fork到自己的Github中

![Preparatory 1](images/readme.preparatory.1.png)

3.在本地安装Git和VS Code  
4.将自己Github中Fork的本项目仓库克隆到本地  

```bash
git clone https://github.com/vFrankwithqq/BCC-PS.git BBC-PS
```

## 总体协作步骤

一共有三个角色：  
项目Owner：对章节进行分工、Merge章节Branch的人  
章节Owner：编写章节内容的人  
校对者：校对章节内容的人  

1. 项目Owner依据确定好的章节，建立每章的章节“Branch”。例如：“part.a”。  
2. 章节Owner将项目Fork到自己的Github上，并在章节“Branch“”上编辑内容。
3. 章节Owner完成内容编写后，将自己编辑的“Branch”“Pull request”到项目仓库对应的“Branch”上。
4. 校对者对“Pull request”进行校对，并在章节Owner的“Pull request”上进行批注、沟通。
5. 章节Owner重新完善章节内容，“Pull request”得到校对者“Approve”后，由项目Owner进行merge操作。

## 参与者协作详细示例

假如，你现在是Part.Test章节的Owner

1. 将BCC-PS仓库克隆至自己的本地，命令如下：  
```powershell
PS> cd $home\documents  #切换到希望本地仓库所存放的路径
PS> git clone https://github.com/vFrankPZhang/BCC-PS.giBBC-PS
```

2. 打开PowerShell，进入仓库“BBC-PS”所在的路径：
```powershell
PS> cd $home\document\BBC-PS
```

3. 执行git pull，将本地的仓库更新至与远端一致
```powershell
PS> git pull
```

4. 查看仓库中有哪些branch
```powershell
PS> git branch -a
master
remotes/origin/HEAD -> origin/master
remotes/origin/master
remotes/origin/part.test
```

5. 切换到part.test分支
```powershell
PS> git checkoupart.test
Switched to branch 'part.test'
```

6. 创建以自己名字为前缀的part.test分支
```powershell
PS> git checkout -you/part.test
Switched to a new branch 'you/part.test'
```

7. 编写内容  
比如你在you/part.test中，新建一个test.md的文件，内test,并保存文件

8. 将文件提交给git来管理
```powershell
PS> git add .
PS> git commit -m 'add test.md'
```

9. 将you/part.test分支推送到Frank's的github上
```powershell
PS> git push
```
如果遇到报错如下：
```powershell
fatal: The current branch you/part.test has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin you/part.test
```
请执行：
```powershell
PS> git push --set-upstream origin you/part.test
```

这时，Frank的github上就会有了you/part.test这个分支

![pull request 1](images/readme.pullrequest.1.png)

10. 将你的分支“you/part.test”pull request给“part.test”，并指定校对者和项目

![pull request 2](images/readme.pullrequest.2.png)

注意，选择好pull request的方向，在这里，你需要把“you/part.test”pull request给“part.test”

![pull request 3](images/readme.pullrequest.3.png)

点击小齿轮，指定校对者和所属项目，并点击“Create pull request”：

![pull request 4](images/readme.pullrequest.4.png)

---
至此，章节的Owner完成了内容的pull request

---

11. 校对者开始对“pull reuqest”进行校对

点击某一行前面的蓝色加号，可以在该行下面，为该行添加批注。

![pull request 5](images/readme.pullrequest.5.png)

![pull request 6](images/readme.pullrequest.6.png)

然后，点击“start a review”开始review。

12. 校对全部完成后，校对者，选择“request change”点击“submit review”，要求章节Owner修改。

![pull request 7](images/readme.pullrequest.7.png)

13. 章节Owner根据批注，修改内容后，重复步骤7-9，“pull request”里面的内容就会更新

14. 章节Owner与校对者，经过多次的沟通、校对，最终完成文档的编写，再由校对人对“review changes”选择“approve”点击“submit review”，完成review。

![pull request 8](images/readme.pullrequest.8.png)

15. “approve”“pull request”后，以为着章节内容已经完成，最后由项目Owner，进行merage操作

![pull request 9](images/readme.pullrequest.9.png)

## 文字稿

### 完成文字稿的具体步骤

1、章的划分、排序，每章目标的说明，及不同章的顺序的逻辑  
2、根据确定的章，确定节的内容纲要  
3、根据节的内容纲要确定内容的标准及要求，如：需要有知识解、截图、练习  
4、分工开始具体写  
5、完成文字稿工作
