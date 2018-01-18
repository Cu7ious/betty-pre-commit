# Automated Betty style checker

This script is a git pre-commit [hook](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks). It automates your C code with both `betty-style` and `betty-doc` by checking your files before you even commit them (can save time!). It runs `betty-style` only for `*.c` files on stage and `betty-doc` for both `*.c` and `*.h`.

<img alt='demo' src='https://cdn.rawgit.com/Cu7ious/betty-pre-commit/d41ab6c3/betty-checker.png?raw=true'>

## Installation


*Prerequesites*
1. Make sure that you have `git` and [betty](https://github.com/holbertonschool/Betty) installed on your machine
2. Make sure you are at the root of you repository (where the `./git` folder is)


**Note:** If you made some pre-commit hooks before, use this line:

```
wget https://raw.githubusercontent.com/Cu7ious/betty-pre-commit/master/pre-commit && echo -e "\n # Betty style checker" >> .git/hooks/pre-commit && tail -n +2 pre-commit >> .git/hooks/pre-commit && rm pre-commit
```

If you don't know what they are, use this one instead:
**Warning:** If you already have hook named pre-commit in the `.git/hooks` of the repo, it will be **SILENTLY REPLACED**

```
wget https://raw.githubusercontent.com/Cu7ious/betty-pre-commit/master/pre-commit && sudo chmod +x pre-commit && mv pre-commit ./.git/hooks
```

## Usage

```
git commit [-m]           # will run both verifications and then if no errors, will do commit
```

```
git commit --no-verify    # will skip checker and proceed to commit
```
