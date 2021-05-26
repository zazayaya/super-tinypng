## 初衷
[tinypng](https://tinypng.com/) 网页版，其实是挺方便的。但是他有上传图片数量的限制，比如每天只能上传 20 张，如果超过这个数量，就会断断续续的出现 `Too many files uploaded at once` 错误 。所以才决定使用 Node 来开发一个绕过数量限制的 npm 包。


## 使用方法
安装：
```bash
# 先安装git命令
# https://git-scm.com/downloads

npm install -g zazayaya/super-tinypng#master
```

然后，在命令行进入到你想要压缩图片的目录，执行：
```bash
super-tinypng
```

## 说明
- tinypng 默认是会对用户上传数量有限制的，使用了 `X-Forwarded-For` 头绕过该限制
- 递归遍历文件夹
- 在当前目录同级目录下创建一个 原始目录名_output 目录，把压缩成功的图片放到对应目录里面
- 新增压缩文件判断，存在的忽略压缩
