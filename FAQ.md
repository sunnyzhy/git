# FAQ

## remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.

生成 token 的步骤:

1. 打开右上角的个人设置页面
2. Settings -> Developer settings -> Personal access tokens -> Generate new token
3. 填写 Note
4. 选择要授予此 token 的范围或权限
   - 要使用 token 访问仓库，请选择 repo
   - 要使用 token 删除仓库，请选择 delete_repo
   - 其他根据需要进行勾选
5. 生成令牌 Generate token
6. 可以把生成的 token (有绿色对号标记的那一段字符串)保存下来
