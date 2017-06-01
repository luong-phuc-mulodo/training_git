# training_git

## Những việc nên làm trước khi push source code 

- Commit phần source code đã có 

```
git add file.txt
git commit -m "message
```

- Thực hiện fetch để xem branch có bị thay đổi gì không 

```
git fetch origin
```

- Nếu branch tại local và branch trên server nằm ở commit khác nhau thì tiến hành pull hoặc rebase

```
git pull origin branch_name
git rebase origin/branch_name
```
