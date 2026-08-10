# Worktree
:git:worktree:

## 1. Clone the repo into a hidden .bare folder
```
git clone --bare git@github.com:user/repo.git .bare
```

## 2. Tell the root folder where the Git history is hidden
```
echo "gitdir: ./.bare" > .git
```

## 3. Fix the fetch configuration to see all remote branches
```
git config remote.origin.fetch "+refs/heads/*:refs/remotes/origin/*"
```

## 4. Create your first worktree (the main branch)
```
git worktree add main
git worktree add <name of the branch>
```

