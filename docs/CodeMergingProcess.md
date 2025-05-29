# 代码合入流程规范
## 一、总体流程
```mermaid
graph LR
    A0[修改并推送特性分支] --> A
    A[创建合并请求] --> A1[DEBUG or 修改检视意见]
    A1 --> B{自动检查}
    B -->|通过| C{人工审核}
    B -->|失败| D[打回]
    C -->|批准| E[合并]
    C -->|拒绝| D
    D --> A1
```
## 二、修改并推送特性分支
```mermaid
graph LR
    A0[找到保护分支] -->|git checkout| A[子特性分支]
    A --> A1[在该分支上进行开发]
    A1 -->|git add && git commit| A2[保存修改]
    A2 -->|git push| A3[上传子特性分支]
```
下面会演示具体流程：<br>
1、先找到保护分支:（开发之前就要明确告知开发人员）<br>
![](../images/CodeMergingProcess/findProtectBranch.png)<br>
2、通过`git`界面创建子分支<br>
```sh
git checkout test_protect_branch
git checkout -b test_developer_personal_branch
```
![](../images/CodeMergingProcess/checkoutNewBranch.png)<br>
3、之后通过`git push`上传分支，如果远端没有此分支，第一次上传需要：
```
git push --set-upstream origin test_developer_personal_branch
```
![](../images/CodeMergingProcess/gitpush.png)<br>

4、做具体的业务代码修改，此处为开发人员的核心工作<br>
5、通过如下命令在自己分支上确认修改并上传
```
git add .
git commit -m "test"
git push
```
此处可以通过git log确认自己的commit生效<br>
![](../images/CodeMergingProcess/gitlog.png)<br>

## 三、创建合并请求
此处直接在界面上演示<br>
![](../images/CodeMergingProcess/createNewMr.png)<br>
![](../images/CodeMergingProcess/SelectBranch.png)<br>
![](../images/CodeMergingProcess/createMR2.png)<br>

## 四、人工审核并合并
此处直接在界面上演示<br>
![](../images/CodeMergingProcess/checkMR.png)<br>
![](../images/CodeMergingProcess/checkMR1.png)<br>
![](../images/CodeMergingProcess/checkMR2.png)<br>
![](../images/CodeMergingProcess/checkMR3.png)<br>
![](../images/CodeMergingProcess/checkMR4.png)<br>
![](../images/CodeMergingProcess/checkMR5.png)<br>