## 撤销commit
在使用git时，偶尔会发现提交的代码有问题，需要回退到上一个版本。  
这里记录以下两种方法，可以实现撤销相关commit的功能。


### reset  
`git reset` 方式不会留下`commit`记录。不加上`--force`会提示版本落后于远程仓库。
````
git reset --hard <HEAD>
git push origin <branch_name> --force
````


### revert
`git revert` 方式会留下一个新的`commit`记录，用以记录撤销了什么内容。相当于直接在代码上做修改并重新`commit`。
````
git revert -n <HEAD>
git commit -m "revert xxx"
````
