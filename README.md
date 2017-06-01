# training_git

## Add Git Tree để view log

git config --global alias.tree "log --oneline --decorate --all --graph"

## Một số lệnh cần biết

- Lấy source từ server về

```
git fetch origin
```

- Update source mới vào branch đang đứng ( ví dụ : branch develop )

```
git pull origin develop
```

NOTE : trường hợp branch local (develop) và branch server (origin/develop) thuộc 2 nhánh khác nhau thì tiến hành rebase hoặc reset

- Để điều hướng branch đến 1 commit nào đó thì thực hiện lệnh rebase ( rebase vào nhánh origin/develop ) , việc này dễ xảy ra conflict nhưng đảm bảo giữ lại source đã thay đổi ở branch hiện tại
```
git rebase origin/develop
```

- Tương tự như lệnh rebase, nhưng sẽ không xảy ra conflict vì tất cả source cũ đều sẽ bị thay đổi theo source rebase
```
git reset --hard origin/develop
```

- Để thay đổi message commit cuối cùng trong trường hợp vẫn chưa push

```
git commit --amend -m "Message mới"
```

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

- Sau đó mới tiến hành push source

```
git push origin branch_name
```
