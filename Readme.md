### 关于文件存放规范

- pages

  该文件夹存放的是要被嵌入的网页

- sources

  该文件夹存放的是您的数据

- static

  该文件存放的是静态数据如css、font、images、js、picture等

  特别的是：js中已经包含了d3, jquery, vega等的js，请编写时尽量用该处的（当然可以不用，只不过我强迫症犯了）

- index.html

  这是首页

  对于替换图片的方法就是搜索”iframe src=“就会找到这7处图片位置了，注意嵌入图片的尺寸。



#### Tips 建议使用pycharm，vscode等，git命令行有点烦

##### git下载与上传

```shell
# first time to use
git clone https://github.com/Friendy0/friendy0.github.io.git

# if you had cloned the project before, do this to refresh your code from remote warehouse.
# git pull https://github.com/Friendy0/friendy0.github.io master

# then you can the thing that you want
# commit your code to your local warehouse?
git commit -m "the message you want to convey"

# git add 新增的文件名
# git restore 修改的文件名

# push to remote
git push https://github.com/Friendy0/friendy0.github.io master
```

##### git报错问题

- [Failed to connect to github.com port 443](https://blog.csdn.net/m0_66695483/article/details/125036055)

  ```shell
  git config --global https.proxy
  git config --global --unset http.proxy
  git config --global --unset https.proxy
  ```

- [fatal: unable to access ‘sshAddress‘: OpenSSL SSL_read: Connection was reset, errno 10054](https://blog.csdn.net/weixin_52914457/article/details/128012212)

  ```shell
  git config --global http.sslVerify "false"
  ```

- [Your branch is ahead of 'origin/master' by 1 commit. ](https://blog.csdn.net/qq_38993096/article/details/105463808?spm=1001.2101.3001.6661.1&utm_medium=distribute.pc_relevant_t0.none-task-blog-2~default~CTRLIST~Rate-1-105463808-blog-79476783.pc_relevant_3mothn_strategy_recovery&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-2~default~CTRLIST~Rate-1-105463808-blog-79476783.pc_relevant_3mothn_strategy_recovery&utm_relevant_index=1)

  ```shell
  git fetch
  ```

- [Your branch is up-to-date with 'origin/master](https://blog.csdn.net/qq_33912215/article/details/89000254)

  ```shell
  git branch 新分支名
  git branch # 检查是否创建成功
  git checkout 新分支名
  git add .
  git commit -m "the message you want to convey"
  git status
  git checkout master
  git merge 新分支名
  git push https://github.com/Friendy0/friendy0.github.io master
  git branch -D 新分支名
  ```

- [git everything up-to-date](https://blog.csdn.net/qldxsun/article/details/80398318)

  ```shell
  git commit -m
  git push
  ```

  
