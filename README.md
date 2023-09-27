# git-pra

## rebase

```
git rebase

git push origin -f
# force push to remote


# id:(N+1)
git rebase -i commit_id
git commit --amend --author="name <mail>"
git rebase --continue
git fetch
git push origin --force-with-lease
# force push to remote (safe)

git reflog
# Q to xeit

git tag <tagname>
git push origin --tags

del
git tag -d <tagname>
git push -d origin <tagname>
```

## git-filter-repo

[git-filter-repo(1) Manual Page](https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html#CALLBACKS)
[git-filter-repo](https://help.aliyun.com/document_detail/206833.html)

```
pip install git-filter-repo

git-filter-repo --name-callback "return name.replace(b'name', b'test')" --force --refs master
# change name in all master

git-filter-repo --name-callback "return name.replace(b'name', b'test')" --force --refs master~2..master
# change name in master~2 and master~

git-filter-repo --email-callback "return email.replace(b'test@mail', b'mail@gmail.com')" --force --refs master~..master
# change email in master~
```