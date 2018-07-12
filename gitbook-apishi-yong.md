# 新建book.json

```
vim book.json
```
# 在book.json中添加使用插件的代码
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
# 页面中使用api主题
```
{% method %}
## Simple method

{% sample lang="request" %}
This text will only appear for JavaScript.

{% sample lang="response" %}
This text will only appear for Go.

{% common %}
This will appear for both JavaScript and Go.
{% endmethod %}
```

以 ` {% method %} ` 作为开始，` {% endmethod %} ` 作为结束；
 ` {% sample lang="request" %} ` 为页签 request 显示内容；
 ` {% sample lang="response" %} ` 为页签 response 显示内容；
 ` {% common %} ` 为两个页签共同显示内容。

> https://github.com/GitbookIO/theme-api
