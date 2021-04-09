

Git Flow Cheatsheet
https://danielkummer.github.io/git-flow-cheatsheet/

Extension
https://github.com/nvie/gitflow

```bash
# Creating feature branches
git flow feature start <name>
git flow feature publish <name>

# Creating releases
git flow release start <name>
git flow release publish <name>

```

## Branches

| Branch | Description |
| --- | --- |
| develop | Default branch, where features / PRs go to |
| main | Last production build |
| hotfix | Need to hotfix something |

## Setup

- Create `develop`, `main` branches
- Make `develop` branch default for each repo
-
