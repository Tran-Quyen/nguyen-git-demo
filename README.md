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

```
git pull origin <remote_branch_name>
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

### Dua tu trang thai commit hien tai ve commit cu hon (Carefully)

```
git revert master
```

```
git revert <commit_id>
```

### Tao nhanh moi co ten la [branch_name] va chuyen sang nhanh do

```
git checkout -b <branch_name>
```

### Chuyen sang nhanh co ten la [branch_name]

```
git checkout  <branch_name>
```

### Kiem tra vi tri branch hien tai

```
git branch
```

### Xoa nhanh

```
git branch -D <branch_name>
```

### Config alias de viet nhanh hon

```
git config --global alias.co checkout
```


### .gitignore

- Giup chung ta danh dau cac file k0 can thiet de push len remote

### Quy trinh lam viec trong thuc te

1. pull code moi nhat ve tu base (master/develop)
2. checkout sang nhanh moi va lam task cua minh
3. git add, commit, push origin [current_branch]
4. Tao Pull Request (PR), Chon nguoi review neu can, chon nhanh gop (master/develop)
5. Tu review lai code, Duoc phe duyet thi merge (Neu co loi thi toi buoc 6)
6. Neu co loi xay ra can fix thi chung ta can:
   1. Ve VSCode xu ly loi
   2. git add, commit --amend -m "message", push origin [current_branch] -f
7. Quay lai buoc 5
8. Can tao PR khac de fix PR truoc (it gap)

### Resolve Conflict:

#### When will conflicts happen?

1. Change same file + same line
2. A deleted file X, B modified file X

#### Method 1: Use Rebase

- Checkout ve master + pull code moi nhat ve
  $ git co master
  $ git pull
- Checkout sang nhanh bi conflict + su dung rebase
  $ git br
  $ git co [conflict_branch]
  $ git br
  $ git rebase master
- Vao Visual Code fix conflict su dung hint
  $ git add .
  $ git rebase --continue
  $ git log --oneline
- Push len github
  $ git push origin [conflict_branch] -f

##### Method 2: Using merge

- Checkout ve master + pull code moi nhat ve
  $ git co master
  $ git pull
- Checkout sang nhanh bi conflict + su dung rebase
  $ git br
  $ git co [conflict_branch]
  $ git br
  $ git merge master
- Vao Visual Code fix conflict su dung hint
  $ git add .
  $ git ci -m "resolve conflict."
- Push len github
  $ git push origin [conflict_branch] -f

