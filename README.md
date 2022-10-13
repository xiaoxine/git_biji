# git

#### 什么是Git
Git 是一个免费的、开源的分布式版本控制系统，可以快速高效地处理从小型到大型的各种项目。  
Git 易于学习，占地面积小，性能极快。  

    版本控制是一种记录文件内容变化，以便将来查阅特定版本修订情况的系统。
    版本控制其实最重要的是可以记录文件修改历史记录，从而让用户能够查看历史版本，方便版本切换。
    为什么需要版本控制：个人开发过渡到团队协作
    


#### Git的三种状态
```
现在请注意，如果你希望后面的学习更顺利，请记住下面这些关于 Git 的概念。 Git 有三种状态，你的文件可能 处于其中之一： 已修改（modified） 和 已暂存（staged）,已提交（committed）。

• 已修改表示修改了文件，但还没保存到数据库中。

• 已暂存表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。

• 已提交表示数据已经安全地保存在本地数据库中。

这会让我们的 Git 项目拥有三个阶段：工作区、暂存区以及 Git 目录。

```

#### 三种状态工作原理

![image](https://user-images.githubusercontent.com/87686120/195655878-853a7584-40ff-489d-9084-e2d2e6c99601.png)

![image](https://user-images.githubusercontent.com/87686120/195655904-4696d0b7-df7b-421b-9b50-64f876b84545.png)
#### 冲突产生的原因： 
    master、hot-fix 其实都是指向具体版本记录的指针。当前所在的分支，其实是由 HEAD决定的。所以创建分支的本质就是多创建一个指针。HEAD 如果指向 master，那么我们现在就在 master 分支上。HEAD 如果执行 hotfix，那么我们现在就在 hotfix 分支上。
    
#### Git 团队协作机制
![image](https://user-images.githubusercontent.com/87686120/195656068-1b4feff7-7fbb-4fc3-aef9-ee0a666c6834.png)

#### git常用命令

    git status 查看本地库状态
    git add hello.txt 添加到暂存区
    git commit -m "日志信息(first commit)" hello.txt 提交到本地库
    git reflog 查看历史记录
    git log 查看详细历史记录
    git reset --hard 版本号（git reflog版本号+鼠标中键复制） 版本穿梭

#### git小乌龟常用
    小乌龟常用菜单：
    TortoiseGit
    	1、add #将新建的文件添加到git列表
    	*2、commit #提交到本地仓库
    	*3、pull #拉取线上仓库代码
    	*4、push #将本地仓库代码推送到线上仓库
    	正常代码提交流程：commit->pull->push
    	*5、show log #查看提交记录
    	
    	*6、Switch/checkout #切换分支
    	7、create Branch #创建分支
    	*8、Merge #合并分支(最容易产生代码冲突)
    		注：pre-release合并master代码
    			使用Merge合并，是把master的代码合并到pre的本地仓库，
    			需要手动push到线上仓库
    		合并方式：
    			1、Branch: #整个分支合并
    			2、commit: #摘取节点进行合并
    				2-1 右上角选择目标分支
    				2-2 选择需要合并的代码节点
    				2-3 点击Cherry Pick this commit
    				2-4 检查节点没有问题点击continue提交
    	
    	9、Revert #回滚代码
    		1、show log打开提交记录
    		2、选择需要回滚的代码节点
    		3、选中上一个提交节点
    		4、点击Reset "分支" to this回滚到当前分支
    		5、弹框->下部分板块(Reset Type)中，选择Hard，点ok
    		6、推送：点击Git sync，勾选弹框中force选项，进行push。
    	
    
#### idea集成Git
#### idea集成Github，Gitee

#### 补充
git init 初始化本地库  
Git 首次安装必须设置一下用户签名，否则无法提交代码

