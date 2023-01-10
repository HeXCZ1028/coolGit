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

## 暂存
#### 暂且当前工作到栈中
`git stash` : 当想切换到其他分支，但当前分支又做了一些修改时，可以使用该命令将当前分支的修改保存到栈中，然后再切换到其他分支

#### 恢复栈中的修改
`git stash pop` 

## 其他
#### 切换分支后，本地文件中的内容也会切换到不同分支的内容，这可能就算Git的高明之处的体现吧.