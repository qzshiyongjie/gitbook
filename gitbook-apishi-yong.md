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
> https://github.com/GitbookIO/theme-api
