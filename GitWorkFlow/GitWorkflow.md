
## 1. 关注ticket的backbone sync状态

BrightAI不想让客户方看到除了BrightAI之外其他的团队，所以BrightAI添加的ticket都是backbone sync状态的，针对这个状态的ticket，需要建立sub task，也就是子任务，此时会生成新的ticket编号。例如从CGCAAI-696创建子任务，生成了CGCAAI-711子任务，此后任务开发或者bug修复，都应基于子任务的ticket编号，来创建对应的分支。

## 2. 根据ticket建立分支

例如ticket编号为CGCAAI-696，则建立task/CGCAAI-696分支。

## 3. 开发功能自测

开发任务或bug解决之后，对功能和业务进行自测。

## 4. 添加单元测试



## 5. swift format

编写的代码，可能会因为SwiftLint产生黄色告警或者红色警告，此时应该使用SwiftFormat来进行代码规范，如下命令，

```
mint run swiftformat
```

## 6. 运行单元测试


提交代码之前，通过Xcode -> Product -> Test(快捷键Command + U)，来运行单元测试。保证单元测试通过。若单元测试不通过，则继续修改单元测试，直到通过为止。


## 7. 提交commit

commit提交有一定的规范，需要带上ticket编号，并且描述本次commit具体解决什么问题。例如`[CGCAAI-696] Request Refund form view,keyboard return key should be next ...`。

## 8. 推送远程分支

将本地修改，提交了commit之后，接着需要将该分支的代码推送到远程服务器。

通过SourceTree的push，选定当前的分支，即可。

因为远程还没有该分支，所以push操作，将会在远程仓库创建对应的远程分支。

## 9. 提交Pull Request


task或feature分支，修改的代码并没有合并到master分支，此时在github的页面，提交一个pull request，添加描述信息，经过团队其他人的代码评审(Code Review)之后，由管理员合并到master分支。


