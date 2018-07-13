## 新建Repositorie并第一次发布到github page
### 将gitbook的md文件提交到主干
1 在www.github.com 新建，比如叫gitbook
2 找到git地址,并用 ` git clone https://github.com/xxx/gitbook.git` 下载到本地
3 执行 `gitbook init `创建book
4 将gitbook 中的 ` SUMMARY.md README.md`复制到Repositorie
6 执行 `gitbook build` 会自动创建`_book` 文件
7 执行 `vim .gitignore`,填写要忽略的文件
```
*~ 
_book
node_modules
```
8 执行 `git init .`
9 执行 `git commit -m "创建gitbook"`
10 执行 `git push`
### 将gitbook的 _book文件夹内容发布到分支
创建 gh-pages 分支
```
$ git checkout --orphan gh-pages
$ git rm --cached -r .
$ git clean -df
$ rm -rf *~
```
执行 `vim .gitignore`,填写要忽略的文件
```
*~ 
_book
node_modules
```
发布_book的内容到gh-pages
```
$ cp -r _book/* .
$ git add .
$ git commit -m "Publish book"
$ git push -u origin gh-pages
```
## 关联gitbook editor
将Repositorie复制到gitbook editor目录底下，我的地址为 `/Users/niuniu/GitBook/Library/Import `
打开gitbook editor，此时

> http://www.chengweiyang.cn/gitbook/github-pages/README.html