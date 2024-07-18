## 简介

DVCS（Distributed Version Control System）：分布式管理系统，在这类系统中，像 Git、Mercurial 以及 Darcs 等，客户端并不只提取最新版本的文件快照， 而是把代码仓库完整地镜像下来，包括完整的历史记录。这么一来，任何一处协同工作用的服务器发生故障，事后都可以用任何一个镜像出来的本地仓库恢复。因为每一次的克隆操作，实际上都是一次对代码仓库的完整备份。
![[截屏2024-07-18 18.52.43.png|450]]


## 通过ssh克隆或推送至Github

[教程](https://blog.csdn.net/weixin_65793170/article/details/128563290?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522172129800316800178518523%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=172129800316800178518523&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-128563290-null-null.142^v100^pc_search_result_base4&utm_term=github%E9%80%9A%E8%BF%87ssh&spm=1018.2226.3001.4187)

## 常用命令

### 本地仓库基本操作

git init 初始化本地仓库
git add 
git commit -m "description" 
git rm -cached 撤销暂存区的修改
git status (- s) 查看工作区 暂存区 本地仓库的状态

***tips***:每次commit其实都是生成一个==***快照***==，每个快照对应一个版本号==***哈希值***==，Head->branch->快照
### 分支操作

git branch -v 查看分支的情况
git branch -d 删除分支
git branch 创建分支

git checkout 切换分支
git checkout -b 创建分支并切换分支

git merge 融合分支（切换到需要融合的分支 后面跟被融合分支名）

### 查看日志

git reflog 查看commit的日志
git log 查看commit的详细日志

### 远程仓库


git remote add <name> <url>
git remote rename <old-name> <new-name>
git remote -v

