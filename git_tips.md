# git版本控制

## 安装git

[下载地址](https://git-scm.com/)

## 常用命令

```bash
## 查看当前变动状态
git status 

## 查看提交版本记录
git log

## 查看本地仓库映射的远程仓库
git branch -vv

## 将当前所有修改添加到stage
git add .

## 提交本地仓库
git commit -m "本次修改的信息"

## 拉取远程仓库
git pull origin [branch name]

## 提交远程仓库
git push origin [branch name]
```

## 操作规范

!> 每次本地commit提交完成后，先拉取远程仓库合并，如有冲突解决冲突后，再commit，然后再push到远程仓库



