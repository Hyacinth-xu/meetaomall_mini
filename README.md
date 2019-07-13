# xcx

> A Mpvue project

## Build Setup

``` bash
# 初始化项目
vue init mpvue/mpvue-quickstart myproject
cd myproject

# 安装依赖
yarn

# 开发时构建
npm dev

# 打包构建
npm build

# 指定平台的开发时构建(微信、百度、头条、支付宝)
npm dev:wx
npm dev:swan
npm dev:tt
npm dev:my

# 指定平台的打包构建
npm build:wx
npm build:swan
npm build:tt
npm build:my

# 生成 bundle 分析报告
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


------------------------------------------------------------------------------------------------------------------------------------------
https://github.com/F-loat/mpvue-router-patch//路由使用 不支持使用 <router-link>

// 字符串
router.push('/pages/news/detail')

// 对象
router.push({ path: '/pages/news/detail' })

// 带查询参数，变成 /pages/news/detail?id=1
router.push({ path: '/pages/news/detail', query: { id: 1 } })

// 切换至 tabBar 页面
router.push({ path: '/pages/news/list', isTab: true })

// 重启至某页面，无需指定是否为 tabBar 页面，但 tabBar 页面无法携带参数
router.push({ path: '/pages/news/list', reLaunch: true })
$router.replace(location, onComplete?, onAbort?, onSuccess?)
关闭当前页面，跳转到应用内的某个页面，相当于 wx.redirectTo，location 参数格式与 $router.push 相似，不支持 isTab 及 reLaunch 属性

$router.go(n)
关闭当前页面，返回上一页面或多级页面，n 为回退层数，默认值为 1

$router.back()
关闭当前页面，返回上一页面

路由信息对象
属性
$route.path
字符串，对应当前路由的路径，总是解析为绝对路径，如 /pages/news/list

$route.params
空对象，小程序不支持该属性

$route.query
一个 key/value 对象，表示 URL 查询参数。例如，对于路径 /pages/news/detail?id=1，则有 $route.query.id == 1，如果没有查询参数，则是个空对象。

$route.hash
空字符串，小程序不支持该属性

$route.fullPath
完成解析后的 URL，包含查询参数和 hash 的完整路径

$route.name
当前路由的名称，由 path 转化而来


------------------------------------------------------------------------------------------------------------------------------------------





npm i mpvue -S//更新依赖
npm i mpvue-template-compiler mpvue-loader mpvue-webpack-target postcss-mpvue-wxss webpack-dev-middleware-hard-disk -S-D


------------------------------------------------------------------------------------------------------------------------------------------

https://developers.weixin.qq.com/miniprogram/dev/framework/open-ability/getPhoneNumber.html//获取手机号
