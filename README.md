# Learn Git

## Cac lenh git thuong duoc su dung

### Clone repository tu remote repository den local repository

```
git clone <remote_repo_url>
```

### Dong bo code tu remote repository ve local repository

```
git pull
```

### Chuyen tu trang thai Changes (Red) => Staged Changes (Green)

```
git add .
```

```
git add *
```

### Kiem tra trang thai cua cac file hien hanh

```
git status
```

### Dua tu trang thai Staged Changes (Green) => COMMITS

```
git commit -m "<message>"
```

### Xem lich su commit

```
git log
```

```
git log --oneline
```

### Day code tu COMMITS => REMOTE REPOSITORY

```
git push -u origin master
```

```
git push
```

```
git push origin master
```

```
git push origin master -f
```

### Xem thong tin commit cu the

```
git show <commit_id>
```

```
gitk
```

### So sanh cac commit

```
git diff <commit_id>
```

```
git diff <commit_id_1> <commit_id_2>
```

### Dua trang thai cac file tu Staged Changes (Green) => Changes (Red)

```
git reset
```

```
git reset <file>
```

```
git restore --staged <file>
```

### Dua tu trang thai COMMITS => Staged Changes (Green)

```
git revert
```

```
git revert <commit_id>
```

