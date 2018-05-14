## 安装
```
npm install zx-ui -S
```
## 使用
``` bash
import Vue from 'vue'
import Zxui from 'zx-ui'
import 'zx-ui/lib/zxhuan.css' 
Vue.use(Zxui)
```
## 查看案例
```
git clone https://github.com/zxhuan/zx-ui.git
cd zx-ui
npm install
npm run start
```
<style>
  .page .content{
    margin:0;
  }
  .iframe-wrap{
    background: url('http://mint-ui.github.io/docs/static/img/phone.5909f66.png') no-repeat center center;
    width:340px;
    height:630px;
    padding:70px 15px 80px;
    background-size:100% 100%;
    box-sizing: border-box;
    position:fixed;
    top:100px;
    right:10px;
  }
   .iframe-wrap .iframe{
    width:100%;
    height:100%;
    background:white;
    border:none;
  }
</style>
<div class="iframe-wrap">
  <iframe src="https://zxhuan.github.io/eg/" class="iframe"></iframe>
</div>