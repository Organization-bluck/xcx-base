# xcx-base
小程序基本框架封装（封装https请求、本地缓存存取等工具函数）（基础版本1.72）


#### wxParse 微信小程序富文本解析组件

[wxParse](https://github.com/icindy/wxParse) 

```
├── README.md           
├── lib                // 第三方相关插件，wxParse 富文本解析组件
├── pages              // 项目文件
├── utils              // 工具函数文件
│   ├── config.js      // 默认配置
│   ├── htmlFormater.js   // 把 html 转为化标准安全的格式
│   ├── util.js        // 封装工具类，封装http 请求，本地缓存
│   └── mock.js        // 本地mock模拟数据
├── index.html         // 项目入口文件
├── project.config.json   // 项目配置文件
├── app.js             // 全局js
├── app.json           // 全局配置
├── app.wxss           // 全局样式
```

#### util 封装函数用法

http

```
util.request({
	url: 'list',
	mock: true,
	data: {
	  tag:'微信热门',
	  start: 1,
	  days: 3,
	  pageSize: 5,
	  langs: 'en'
	}
	}).then(res => {
    // do something
  })
```

Storage

```
util.setStorageData('_key_', value, () => {
  // do success something
});
```

