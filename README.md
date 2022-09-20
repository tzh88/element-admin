<p align="center">
  <a href="https://github.com/vuejs/vue">
    <img src="https://img.shields.io/badge/vue-2.5.17-brightgreen.svg" alt="vue">
  </a>
  <a href="https://github.com/ElemeFE/element">
    <img src="https://img.shields.io/badge/element--ui-2.4.6-brightgreen.svg" alt="element-ui">
  </a>
  <a href="https://travis-ci.org/umi-soft/element-admin" rel="nofollow">
    <img src="https://travis-ci.org/umi-soft/element-admin.svg?branch=master" alt="Build Status">
  </a>
  <a href="https://github.com/umi-soft/element-admin/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/mashape/apistatus.svg" alt="license">
  </a>
  <a href="https://github.com/umi-soft/element-admin/releases">
    <img src="https://img.shields.io/github/release/umi-soft/element-admin.svg" alt="GitHub release">
  </a>
</p>

## Getting started

```bash
# clone the project
git clone https://github.com/umi-soft/element-admin.git

# install dependency
npm install

# develop
npm run dev
```

## Build

```bash
# build for test environment
npm run build:sit

# build for production environment
npm run build:prod
```

## Online
[Preview](http://umi-soft.github.io/element-admin)

## Browsers support

Modern browsers and Internet Explorer 10+.

| [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png" alt="IE / Edge" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>IE / Edge | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png" alt="Firefox" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Firefox | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png" alt="Chrome" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Chrome | [<img src="https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png" alt="Safari" width="24px" height="24px" />](http://godban.github.io/browsers-support-badges/)</br>Safari |
| --------- | --------- | --------- | --------- |
| IE10, IE11, Edge| last 2 versions| last 2 versions| last 2 versions

## 2.x计划

- 提供更多的页面布局模板，目前仅一种模板
- 提供后端spring-boot开源工程
- 微调数据库字段设计，比如废弃state字段，flag字段调整为deleted，增加后端API安全资源表等等
- 升级vue-cli至3.x

## License

[MIT](https://github.com/umi-soft/element-admin/blob/master/LICENSE)


## tzh笔记
#1.import Qs from 'Qs'  => import Qs from 'qs'

#2. proxy: {
      '/admin': {
        target: `http://localhost:${port}/mock`,
        // target: 'http://localhost:8080',
        changeOrigin: true,
        pathRewrite: {
          '^/' : '/'
        }
      }
    }
    
  ps：target改成mock
#3.  loginByLoginName: config => {
    console.log(config)
    console.log(Qs.parse(config.body))
    // const params = JSON.parse(config.body)
    const params =Qs.parse(config.body)
    ps:JSON.parse(config.body) -> Qs.parse(config.body)(QS用来对象互转url字符串)


