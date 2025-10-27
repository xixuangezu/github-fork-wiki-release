[English](./README.md) / [中文](./README_CN.md)

# Introduction

Quickly Fork All Wiki and Release Resources on GitHub

As is well known, forking a GitHub project does not include its wiki and release. This GitHub Action helps you quickly fork all contents.

# How to Use

#### 1. Create Wiki in the Forked Repository

- Go to your project page -> Wiki tab -> Create the first page -> Save

#### 2. Start Forking Wiki and Release Resources

- Copy `.github` to your own forked repo and push -> Go to project page -> Actions tab -> I understand -> Fork Release and Wiki -> Run workflow

# Common Errors

#####  ! [remote rejected]   6.33 -> 6.33 (refusing to allow a GitHub App to create or update workflow `.github/workflows/build.yml` without `workflows` permission)
Reason: Workflows were modified in tags, but Action doesn’t have workflow read/write permission.

- Click your avatar -> Settings -> Developer Settings -> Personal access tokens -> Tokens -> Generate new token -> Generate new token (classic)
  - Note: PAT_TOKEN
  - Check repo, workflow, admin:org
 -> Click Generate token -> Copy the generated token

- Project page -> Settings -> Secrets and variables -> Actions -> Repository secrets
  - Paste the generated PAT_TOKEN
 -> Add secret

##### HTTP 403: API rate limit exceeded for user ID 22230479.
Reason: Too many GH CLI requests.

Wait for one hour.
