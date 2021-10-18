# git 还原修改

- 只是修改了文件，没有任何 git 操作
   ```bash
   git checkout -- xxx.java            // 还原 xxx.java 文件
   git checkout -- *            // 还原所有文件
   ```

- 修改了文件，并提交到暂存区（即：编辑之后, 进行 git add, 但没有 git commit -m "xxx"）
   ```bash
   git log --oneline            // 可以省略
   git reset HEAD               // 回退到当前版本
   git checkout -- xxx.java
   ```

- 修改了文件，并提交到仓库区（即：编辑之后, 进行 git add 并且 git commit -m "xxx"）
   ```bash
   git log --oneline            // 可以省略
   git reset HEAD^            // 回退到上一个版本，注意 HEAD 后面有个 ^; HEAD^: 回退到上个版本; HEAD^^: 回退到上上个版本; HEAD~版本号: 回退到指定版本
   git checkout -- xxx.java
   ```
