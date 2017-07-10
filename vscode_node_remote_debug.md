node --debug=5858 app.js
 
--debug-brk
选项用于让程序停止在程序源码的第一行。

lanchu.json添加配置

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "AttachCloud",
            "type": "node",
            "request": "attach",
            "port": 5858,
            "address": "＊＊＊IP地址＊＊＊",
            "restart": true,
            "sourceMaps": false,
            "outDir": null,
            "localRoot": "${workspaceRoot}",
            "remoteRoot": "/app"
        }
    ]
}
```
