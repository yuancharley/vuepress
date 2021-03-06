# GitFlow工作流指南

## 项目经理：

1. 在git等远程仓库中创建项目，并且初始化项目，即完成master分支在远程的创建。

2. git clone拉取代码至本地，完成本地master分支的创建。

3. 基于head的master分支创建develop分支

4. 切换至develop，推送至远程仓库

   

## 小组开发人员：

1.  clone项目至本地仓库，自动在本地创建master分支代码

2. 切换至远程develop分支，创建本地develop分支

3. 基于develop创建功能分支，并切换至功能分支

4. 进行开发，代码提交、推送

5. 在远程仓库界面中将功能分支创建合并请求至develop分支

6. 项目经理确认合并请求完成功能分支合并至develop分支。

   

当develop分支开发到一定阶段后，将develop分支进行合并创建预发布版本（由需要进行发布的组员操作）

1. 切换至develop分支，进行代码拉取

2. 在本地仓库基于develop分支创建预发布分支（如release-1.0.0）

3. 推送至远程仓库

4. 创建合并请求至远程仓库的master分支

5. 项目经理确认合并master分支请求

   

切换至本地master分支，进行打标签

1. 切换至本地master分支
2. 拉取项目代码
3. 基于master分支创建标签（注意标签名称，版本语义规范，如1.0.0-RELEASE）
4. 推送至远程仓库



如果1.0.0-RELEASE该版本有bug

1. 在远程仓库界面中创建Issues，并记住#后面的数字
2. 修复bug的组员基于有bug的发行标签版本1.0.0-RELEASE创建修复版本（hotfix_0004，此处4为上步记住的数字）
3. 修复bug，提交并推送
4. 创建合并请求至远程仓库的master
5. 项目经理确认合并master分支请求
6. 组员进master分支进行拉取
7. 创建新版标签1.0.1-RELEASE
8. 推送至远程仓库
9. 删除本地仓库及远程仓库的功能分支、预发布分支、hotfix分支
10. 完成。