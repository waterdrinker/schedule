schedule
=============

工作计划


## 1. default app

参数:

 * -b, --bind host:port
 * -k, --key key file path
 * -w, --worker async(gevent), sync(socketserver)
 * --git-path git command path
 * --repo-path git repository root path

 还有一些在 config.py 里面

`maria -b host:port -k host.key --git-path=/usr/local/git --repo-path=./`


## 2. 指定 app

app 内可以设置 Hook，但是如果命令行也设置同样的参数了，可以以命令行为准。

`maria -b host:port app.wsgi:application`
