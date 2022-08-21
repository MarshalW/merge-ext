# Merge test

测试多个 repo 下分支的合并.

从 https://github.com/MarshalW/merge-test main 分支合并改动到当前 main 分支。

```bash
# 创建临时空分支
git checkout --orphan test_tmp
git reset --hard

# 当前空分支下pull指定repo的branch
git pull https://github.com/MarshalW/merge-test.git main

# 切换到main分支，做merge
git checkout main
git merge test_tmp

# 删除临时分支
git branch -d test_tmp
```
