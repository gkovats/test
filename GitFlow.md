

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
- Protect `develop` and `main` branches

## Repo Problems

**1. Patch Management**

We don't have a running master on WCMS, so each time we come up with a new structure. We create a branch from the last tag, which gets a little tedious each time. Even more when each patch branch needs to do the same - find the string in the midst of 6000 tags that's the last release.

**2. Environments for patches**

We have test-br, but TP isn't set up to build to it, and right now you need two WCMS builds to get to test-br.

**3. Feature branches often need cherry picking**

Having a standing `main` branch can help with this, folks will have a constant branch to use.

## Jenkins Problems

Test



- **WCMS**:
  - Push: dev -> test -> stage -> prod
    - No one uses dev as intended, it just adds 20 minutes to a test build
  - too many tags
    - There's currently 4,800+ tags
  - Automate dev builds somehow
- **TP**:
  - Too many jobs. Reduce to one for each environment with options, maybe an extra for environments we support but don't update often
  - Targets aren't clear. Need better way of labelling specific, checkboxes ideal
