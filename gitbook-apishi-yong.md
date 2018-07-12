# 新建book.json
```
vim book.json
```
#在book.json中添加使用插件的代码
```
{
  "plugins": ["theme-api"],
  "pluginsConfig": {
    "theme-api": {
        "split": true,
      "languages": [
        {
          "lang": "request",
          "name": "请求参数",
          "default": true
        },
        {
          "lang": "response",
          "name": "返回结果"
        }
      ]
    }
  }
}
```

> https://github.com/GitbookIO/theme-api
