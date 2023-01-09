## 查看

#### 查看当前所有分支
`git branch `

#### 创建新分支
`git branch <newBranchName>`

#### 切换到其他分支
`git checkout <otherBranch>`
`git switch <otherBranch>` (推荐)

#### 创建新分支,并切换到新分支
`git checkout -b <newBranchName>`
`git switch -c <newBranchName>` (推荐)

## 删除
#### 删除本地分支
`git branch -d <branchName>`

#### 删除远程分支
`git push origin --delete <branchName>`