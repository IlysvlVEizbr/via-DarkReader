# via-DarkReader
测试中：尝试把DarkReader用在via浏览器
- 源码基于 [darkreader / ©darkreader / MIT](https://github.com/darkreader/darkreader) 修改
- 原理：借用jsdelivr加速，导入一个修改过，能立即启动的DarkReader.js

-----

## 脚本使用示例
```javascript
// ==UserScript==
// @name         DarkReader
// @description  js脚本实现夜间模式
// @author       Sky
// @version      1.0.1
// @run-at       document-start
// @match        *://*/*
// @grant        unsafeWindow
// @homepageURL  http://via-app.cn/#/pluginDetail/53
// @namespace    https://viayoo.com/
// ==/UserScript==
(function(){const w = window;
/*以下参数可修改，推荐取值范围1~100，=null表示恢复默认值*/
w.DR_setting0=100; /*亮度*/
w.DR_setting1=90; /*对比度*/
w.DR_setting2=10; /*滤蓝光程度*/
/*－－－－以下勿改－－－－*/
try{const lib=document.createElement('script');lib.src='https://cdn.jsdelivr.net/gh/IlysvlVEizbr/via-DarkReader@1.0.1/DarkReader.js';lib.defer=true;document.body.append(lib);}catch(err){console.log('DarkReader：',err);}})();
```
