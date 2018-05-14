## cell
```html
<template>
  <div class="cell">
    <zx-cell-group title="有标题">
      <zx-cell-item border>
        <span name='left'>左边</span>
        <span name='right'>右边</span>
      </zx-cell-item>
      <zx-cell-item border arrow type='label'>
        <span name='left'>左边</span>
        <span name='right'>type:label</span>
      </zx-cell-item>
      <zx-cell-item border arrow>
        <span name='left'>左边</span>
        <span name='right'>type:defalut</span>
      </zx-cell-item>
      <zx-cell-item border arrow type='link' href='/'>
        <span name='left'>链接</span>
        <span name='right'>type:link</span>
      </zx-cell-item>
    </zx-cell-group>
  </div>
</template>
<script>
  export default {
    name: 'cell',
    data() {
      return {};
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
  <iframe src="https://zxhuan.github.io/eg/#/cell" class="iframe"></iframe>
</div>

## zx-cell-group Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
title | 标题| string| - |空
## zx-cell-item Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
border | 底边框| boolean| true,false |false
arrow  | 右侧箭头| boolean| true,false |false
type  | 类型|string|link,label|label
href  | 要跳转的路由|string|-|-
