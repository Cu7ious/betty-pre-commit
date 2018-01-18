# Automated Betty style checker

This script is a git pre-commit (hook)[https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks]. It automates your C code with both `betty-style` and `betty-doc` by checking your files before you even commit them (can save time!). It runs `betty-style` only for `*.c` files on stage and `betty-doc` for both `*.c` and `*.h`.

## Installation

*Note:* If you made some pre-commit hooks before, use this line:

```
wget https://raw.githubusercontent.com/Cu7ious/betty-pre-commit/master/pre-commit && && echo -e "\n # Betty style checker" && tail -n +2 >> ./git/hooks/pre-commit && rm pre-commit
```

If you don't know what they are, use this one instead:

```
wget https://raw.githubusercontent.com/Cu7ious/betty-pre-commit/master/pre-commit && mv pre-commit ./git/hooks
```

## Usage

```
git commit [-m]           # will run both verifications and then if no errors, will do commit
```

```
git commit --no-verify    # will skip checker and proceed to commit
```
