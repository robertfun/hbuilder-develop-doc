# 开发环境安装

## 安装nodejs

去[中文官网](中文官网),下载LTS版本

## 安装cnpm

cnpm是使用淘宝镜像源安装node module的工具，在命令行工具中执行一下命令，

```bash
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

## 克隆项目后的操作

项目的机构分为，gulp，mockApiData(可能没有)

* 进入 gulp 目录，执行`cnpm install`, 安装完毕后，在当前gulp目录，执行 `gulp` , 就可以开发了

* 如果需要模拟数据，可以进入 mockApiData，执行`cnpm install`, 安装完毕后，在当前mockApiData，执行目录，执行 `npm run dev`
；mock数据在当前Apis目录下，建立自己需要的json文件，参考其它目录中的json文件即可

!> mock数据时，因为涉及到跨域访问，如需在pc上调试，每个api请加上对应的 options方法，如以下实例;如果是真机或者模拟器调试则不需要加，mui.ajax默认使用native去请求

```js
"api": {
    "GET  /api/aaa": {
        "request": {
            "querystring": {
                "keyword": "2", 
                "currentPage": 10
            }
        },
        "response": {
            "list": [
                {
                    "id": 1,
                    "time": "2016.05.06",
                    "area": "500",
                    "price": "50000"
                },
                {
                    "id": 2,
                    "time": "2016.05.06",
                    "area": "500",
                    "price": "50000"
                }
            ]
        }
    },
    "OPTIONS  /api/aaa": {
        "response": {}
    }
}
```


