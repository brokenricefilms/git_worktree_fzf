# git worktree fzf with my 🫰

- I'm test it worked on bash maybe zsh will work.
- Fish and other shell can be support later if i not lazy, pull request are welcome🫰

## Install

```bash
 curl --remote-name https://raw.githubusercontent.com/thuanowa/git_worktree_fzf/master/git_worktree_fzf.bash > ~/.local/share/git_worktree_fzf.bash

 echo "source ~/.local/share/git_worktree_fzf.bash" >> ~/.bashrc
 ```

OR

- Just add this [git_worktree_fzf.bash](./git_worktree_fzf.bash) on your bash config

## How to use?

worktree will be stored at `.worktrees`:

```bash
git_folder
--- README.md
--- .worktrees/feat/here
--- .worktrees/tmp
```

**Ignore `.worktrees/` globally**

> ~/.gitconfig
```bash
[core]
excludesfile = ~/.gitignore
```

> ~/.gitignore
```bash
.worktrees/
```

**Function**

- The script have 2 functions:
    1. fzf_git_worktree_change_dir
    2. fzf_git_worktree_remove
- you can make the alias of that like me.

```bash
alias w="hzf_git_worktree_change_dir"
alias ww="fzf_git_worktree_remove"
```

### fzf_git_worktree_change_dir

- Show all your git worktree
- Search your worktrees with fzf
1. if had, change dir to your worktree location
2. if the name of worktree you type don't have -> just press `enter` it will create new git worktree with the name you provice for you.

### fzf_git_worktree_remove

- Show all your git worktree
- Search your worktrees with fzf, find the worktree you want remove, press enter will remove this worktree
