# ua-device [![Build Status](https://travis-ci.org/fex-team/ua-device.svg?branch=master)](https://travis-ci.org/fex-team/ua-device) [![download](https://img.shields.io/npm/dt/ua-device.svg)](https://www.npmjs.com/package/ua-device) [![version](https://img.shields.io/npm/v/ua-device.svg)](https://www.npmjs.com/package/ua-device)

一个用于解析UA来得到用户终端信息的JS库，详情可见[线上demo](http://fex-team.github.io/ua-device/)

## 下载
```bash
npm install @ali/vmate-ua-device
```


## 目录结构
```
@ali/vmate-ua-device/
├── LICENSE
├── README.md
├── index.js
├── lib
│   ├── ua-device.js
│   └── useragent-base.js
├── package.json
└── test
    ├── index.js
    ├── test_input
    └── treemap.js
```

## 测试

```bash
npm test

# you can get the test result like this:
#  ua-device测试数据共22848条
  # ✓ browser_name识别成功共 53580 条，成功率为 99.85%

  # ✓ browser_version识别成功共 53384 条，成功率为 99.48%

  # ✓ engine_name识别成功共 53434 条，成功率为 99.57%

  # ✓ engine_version识别成功共 53431 条，成功率为 99.57%

  # ✓ os_name识别成功共 53403 条，成功率为 99.52%

  # ✓ os_version识别成功共 52521 条，成功率为 97.87%

  # ✓ device_manufacturer识别成功共 42115 条，成功率为 78.48%

  # ✓ device_model识别成功共 51503 条，成功率为 95.97%
```
有兴趣的同学可以将`ua-device`与其它高star库进行对比，相信对比后无论在识别成功率还是识别内容的准确性上，你都会选择`ua-device`。


## 调用方式

```javascript
var UA = require('@ali/vmate-ua-device');
var input = 'Mozilla/5.0 (iPhone; U; CPU iPhone OS 5_1_1 like Mac OS X; en) AppleWebKit/534.46.0 (KHTML, like Gecko) CriOS/19.0.1084.60 Mobile/9B206 Safari/7534.48.3';

var output = new UA(input);
console.log(output);

// you can get a json like this:
// {
//     browser: {  //浏览器信息
//         name: 'Chrome',
//         version: {
//             original: '19.0.1084.60',
//         }
//     },
//     engine: {   //浏览器内核
//         name: 'Webkit',
//         version: {
//             original: '534.46.0',
//         }
//     },
//     os: {       //操作系统
//         name: 'iOS',
//         version: {
//             original: '5.1.1',
//         }
//     },
//     device: {   //硬件信息
//         type: 'mobile',
//         manufacturer: 'Apple',
//         model: 'IPHONE'
//     }
// }
```
