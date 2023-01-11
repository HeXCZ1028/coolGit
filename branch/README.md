## 查看

#### 查看当前所有分支
`git branch `

#### 创建新分支
`git branch <newBranchName>`： 基于当前所在的分支,创建一个新分支. 新分支内容和当前分支内容一样,连暂存区，工作区等都一样.

#### 切换到其他分支
`git checkout <otherBranch>`
`git switch <otherBranch>` (推荐)

#### 创建新分支,并切换到新分支
`git checkout -b <newBranchName>`
`git switch -c <newBranchName>` (推荐)

## 删除
#### 删除本地分支
`git branch -d <branchName>`

#### 强制删除本地分支
`git branch -D <branchName>`

#### 删除远程分支
`git push origin --delete <branchName>`

## 暂存与恢复
#### 暂且当前工作到栈中
`git stash` : 当想切换到其他分支，但当前分支又做了一些修改时，可以使用该命令将当前分支的修改保存到栈中，然后再切换到其他分支

#### 恢复栈中的修改
`git stash pop` 

#### 恢复到修改之前
`git checkout -- <fileName>` : 当还未将变更从工作区加入到暂存区时，可以使用该命令放弃所做的修改（对新建文件无效）

#### 模块与子模块
模块和子模块在git命令上相互独立，比如在模块中切换分支，并不会在子模块中切换，需要在子模块中同样切换分支.
`git submodule foreach --recursive` : 当项目中有子模块时，可以用该命令对所有子模块同步一个命令。
`git submodule foreach --recursive git switch <branchName>` : 比如切换分支

## 其他
#### 切换分支后，本地文件中的内容也会切换到不同分支的内容，这可能就算Git的高明之处的体现吧.