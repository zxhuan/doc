## tab
```html
<template>
  <div class="tab">
    <zx-tab v-model='active'>
      <zx-tab-item label='选项卡一' name='tab1'>
        选项卡一
      </zx-tab-item>
      <zx-tab-item label='选项卡二3' name='tab2'>
        选项卡二
      </zx-tab-item>
      <zx-tab-item label='选项卡三12' name='tab3'>
        选项卡三
      </zx-tab-item>
    </zx-tab>
    <div style="margin: 20px 0;border: 0.5px solid rgb(247, 247, 247)"></div>
    <zx-tab v-model='active'  :postion="'left'">
      <zx-tab-item label='选项卡一' name='tab1'>
        选项卡一
      </zx-tab-item>
      <zx-tab-item label='选项卡二3' name='tab2'>
        选项卡二
      </zx-tab-item>
      <zx-tab-item label='选项卡三12' name='tab3'>
        选项卡三
      </zx-tab-item>
    </zx-tab>
    <div style="margin: 20px 0;border: 0.5px solid rgb(247, 247, 247)"></div>
    <zx-tab v-model='active' :postion="'right'">
      <zx-tab-item label='选项卡一' name='tab1'>
        选项卡一
      </zx-tab-item>
      <zx-tab-item label='选项卡二3' name='tab2'>
        选项卡二
      </zx-tab-item>
      <zx-tab-item label='选项卡三12' name='tab3'>
        选项卡三
      </zx-tab-item>
    </zx-tab>
  </div>
</template>
<script>
  export default {
    name: 'tab',
    data() {
      return {
        active: 'tab1'
      };
    }
  };
</script>
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
  <iframe src="https://zxhuan.github.io/eg/#/tab" class="iframe"></iframe>
</div>


## zx-tab Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
value| 值| string,number|-|必填
postion| tab定位| string|top,left,right|top

## zx-tab-item Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
label| tab标题| string|-|必填
name| name鱼zx-tab value 值队形| string|-|必填
