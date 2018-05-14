# button
```html
<template>
  <div class="button">
    <zx-button type='primary'>primary</zx-button>
    <zx-button type='success'>success</zx-button>
    <zx-button type='info'>info</zx-button>
    <zx-button type='warning'>warning</zx-button>
    <zx-button type='danger'>danger</zx-button>
    <zx-button type='primary' size='mini'>button mini</zx-button>
    <zx-button type='primary' size='large'>{{largeButton}}</zx-button>
    <zx-button type='primary' @click="clickFn" flex>click button</zx-button>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        largeButton: 'large button'
      };
    },
    methods: {
      clickFn() {
        this.largeButton = 'this is large button';
      }
    },
    created() {
      this.$store.dispatch('setTtile', 'button');
    }
  };
</script>
<style scoped>
  .button {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 10px;
  }

  .zx-button {
    margin-bottom: 10px;
  }
</style>
```
# zx-button Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
type | 类型| string| primary,success,info,warning,danger,primary |info
size| 尺寸|string|defalut,large,min|defalut

# zx-button Events

事件名称 | 说明|回调参数
---|---|---
click | 点击事件|回调event

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
  <iframe src="https://zxhuan.github.io/eg/#/button" class="iframe"></iframe>
</div>