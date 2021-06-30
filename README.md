# Create other Repository Branch Action

[![Action test on Ubuntu](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/ubuntu_test_action.yml/badge.svg)](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/ubuntu_test_action.yml) [![Action test on MacOS](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/macos_test_action.yml/badge.svg)](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/macos_test_action.yml) [![Action test on Windows](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/windows_test_action.yml/badge.svg)](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/actions/workflows/windows_test_action.yml)

Github Action to create a new branch on another repository 🚀📦

* * *

## 📚 Usage

☞ [Who is using this action? 🧑‍💻](https://github.com/search?q=GuillaumeFalourd+create-other-repo-branch-action+path%3A.github%2Fworkflows+language%3AYAML&type=code)

### How does the action work?

## ♻️ Scenarios

_⚠️ Don't use this action to create a branch from the same repository. To do so, [other actions on the marketplace are more efficient](https://github.com/marketplace?type=actions&query=create+branch+)._

### Creating new branch on another repository using `default branch` as reference

```yaml
    steps:
      - uses: GuillaumeFalourd/create-other-repo-branch-action@main
        with:
          repository_owner: GuillaumeFalourd
          repository_name: poc-github-actions
          new_branch_name: release-1.2.3
          access_token: ${{ secrets.ACCESS_TOKEN}}
```

### Creating new branch on another repository using `a specific branch` as reference

```yaml
    steps:
      - uses: GuillaumeFalourd/create-other-repo-branch-action@main
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
**new_branch_ref** | NO | Reference to create the new branch name on other repository <br/> _e.g: `main` (the `default branch` is used if not informed)_
**access_token** | NO | A [PAT](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token) that has access to the repository (if necessary)._

* * *

## 🤝 Contributing

☞ [Guidelines](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/blob/main/CONTRIBUTING.md)

## 🏅 Licensed

☞ This repository uses the [Apache License 2.0](https://github.com/GuillaumeFalourd/create-other-repo-branch-action/blob/main/LICENSE)
