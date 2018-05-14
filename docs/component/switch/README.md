# switch
```html
<template>
  <div class="switch">
    <div class="box" style="margin-bottom: 10px;">
      <zx-switch v-model='values' @change="changevalue(values)" active-text="开" inactive-text="关"></zx-switch>
    </div>
    <div class="box">
      <zx-switch v-model='value' @change="changevalue(value)" active-color="#019dfa" inactive-color="#a3b5bf"></zx-switch>
    </div>
    <div class="box">
      <zx-switch v-model='value1' @change="changevalue(value1)" active-color="#009688" inactive-color="#e9eaea" active-text="hello"
        inactive-text="world"></zx-switch>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        values: true,
        value: false,
        value1: false
      };
    },
    methods: {
      changevalue(values) {
        console.log(values);
      }
    },
    created() {
    }
  };
</script>
<style scoped lang="scss">
  .switch {
    padding: 1rem;
  }
</style>
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
  <iframe src="https://zxhuan.github.io/eg/#/switch" class="iframe"></iframe>
</div>

## zx-switch Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
value| 值| string,number|-|必填
active-text |打开时的文字描述|string|-|空
inactive-text |关闭时的文字描述|string|-|空
active-color |打开时的背景色|string|-|#019dfa
inactive-color |关闭时的背景色|string|-|#ffffff

## zx-switch Events
事件名称 | 说明|回调参数
---|---|---
change | change事件|回调event