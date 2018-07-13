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
1 将Repositorie复制到gitbook editor目录底下，我的地址为 `/Users/niuniu/GitBook/Library/Import `
2 打开gitbook editor，此时gitbook editor底下已有 book ，直接打开，我尝试过登入，一直登入失败。
3 点击右上角导航栏，点击 Book ,点击 Repository Settings ，复制主干的git地址，这样就可以直接用gitbook editor编辑了
4 编写完直接点击左上角同步就行了
## book编辑后把重新发布到github page
未使用gitbook editor 提交编辑的md文件到主干，使用时可以使用gitbook editor直接同步
```
git checkout master
git add .
git commit -m '修改内容'
git push
```
## 更新_book文件内容到github page
```
git checkout master
gitbook build
git checkout gh-pages
cp -r _book/* .
git add .
git commit -m "修改内容"
git push
```

> http://www.chengweiyang.cn/gitbook/github-pages/README.html