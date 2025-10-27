[English](./README.md) / [中文](./README_CN.md)

# 简介

github 快速 Fork 所有 wiki 和 release资源

众所周知github fork项目不会fork wiki和release。这里提供了一个github action帮助快速fork所有内容

# 使用方法

#### 1.在fork的仓库创建wiki

- 项目页顶部 -> wiki -> create the first page -> save

#### 2.开始 Fork wiki 和 release资源

- 把.github复制到本人fork的仓库 并push -> 项目页顶部 -> Action -> I understand -> 同步上游 Release 与 Wiki -> run workflow


# 常见错误

##### ! [remote rejected]   6.33 -> 6.33 (refusing to allow a GitHub App to create or update workflow `.github/workflows/build.yml` without `workflows` permission)
原因：tag中修改过workflows，Action没有添加workflow读写权限

- 用户头像 -> setting -> Developer Settings -> Personal access tokens -> tokens -> Generte new token -> Generte new token(classic)
  - Note：PAT_TOKEN
  - 勾选 repo workflow admin:org
 -> 点击 Generte token -> 复制生成的tokens

- 项目页顶部 -> settings -> Secrets and variables -> Actions -> Repository secrets
  - 填入刚才生成的PAT_TOKEN
 -> add secrets

##### HTTP 403: API rate limit exceeded for user ID 22230479.
原因：GH CLI调用次数超标

等待一个小时