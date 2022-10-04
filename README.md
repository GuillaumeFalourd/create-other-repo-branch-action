# Create Other Repo Branch Action

[![Public workflows that use this action.](https://img.shields.io/endpoint?url=https%3A%2F%2Fapi-endbug.vercel.app%2Fapi%2Fgithub-actions%2Fused-by%3Faction%3DGuillaumeFalourd%2Fcreate-other-repo-branch-action%26badge%3Dtrue)](https://github.com/search?o=desc&q=GuillaumeFalourd+create-other-repo-branch-action+path%3A.github%2Fworkflows+language%3AYAML&s=&type=Code) [![Action test on Ubuntu](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/ubuntu_test_action.yml/badge.svg)](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/ubuntu_test_action.yml) [![Action test on MacOS](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/macos_test_action.yml/badge.svg)](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/macos_test_action.yml) [![Action test on Windows](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/windows_test_action.yml/badge.svg)](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/windows_test_action.yml)

![title](https://user-images.githubusercontent.com/22433243/124029399-7d608c80-d9cb-11eb-9f78-48524007ac3d.png)

Github Action to create a new branch on another repository 🆕🚀

* * *

## 📚 Usage

## ⚙️ How does the action work?

_⚠️  Don't use this action to create a branch on the same repository! To do so, [other actions on the marketplace are more efficient](https://github.com/marketplace?type=actions&query=create+branch+). You can also do it with the [actions/checkout](https://github.com/actions/checkout) and `git` commands._

### ♻️ Scenarios

#### Creating new branch on another repository using `default branch` as reference

```yaml
    steps:
      - uses: GuillaumeFalourd/create-other-repo-branch-action@v1.2
        with:
          repository_owner: GuillaumeFalourd
          repository_name: poc-github-actions
          new_branch_name: release-1.2.3
          access_token: ${{ secrets.ACCESS_TOKEN}}
```

#### Creating new branch on another repository using `a specific branch` as reference

```yaml
    steps:
      - uses: GuillaumeFalourd/create-other-repo-branch-action@v1.2
        with:
          repository_owner: GuillaumeFalourd
          repository_name: poc-github-actions
          new_branch_name: release-1.2.3
          new_branch_ref: release-candidate
          access_token: ${{ secrets.ACCESS_TOKEN}}
```

* * *

## ▶️ Action Inputs

Field | Mandatory | Observation
------------ | ------------  | -------------
**repository_owner** | YES | Repository Owner <br/> _e.g: `octocat`_
**repository_name** | YES | Repository Name <br/> _e.g: `my-repo-name`_
**new_branch_name** | YES | New branch name created on other repository <br/> _e.g: `release-*.*.*`_
**new_branch_ref** | NO | Reference to create the new branch name on other repository <br/> _e.g: `release-candidate` (the `default branch` is used if not informed)_
**access_token** | NO | A [PAT](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token) that has access to the repository (if necessary).
**ignore_branch_exists** | NO | This (boolean) field will gracefully skip branch creation if the requested branch already exists <br/> _e.g: `true`_

* * *

## 🤝 Contributing

☞ [Guidelines](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/blob/main/CONTRIBUTING.md)

## 🏅 Licensed

☞ This repository uses the [Apache License 2.0](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/blob/main/LICENSE)
