## select
```html
<template>
  <div class="select">
    <zx-form-group>
      <zx-select v-model='selectValue' place='请选择选项'>
        <zx-option value='1'>选项卡1</zx-option>
        <zx-option value='2'>选项卡2</zx-option>
        <zx-option value='3'>选项卡3</zx-option>
        <zx-option value='4'>选项卡4</zx-option>
      </zx-select>
    </zx-form-group>
    <zx-form-group title='地址'>
      <zx-select v-model='selectAddress' place='请选择地址' @change='changeValue(selectAddress)'>
        <zx-option value='1'>北京</zx-option>
        <zx-option value='2'>上海</zx-option>
        <zx-option value='3'>广州</zx-option>
        <zx-option value='4'>天河</zx-option>
      </zx-select>
    </zx-form-group>
    <p>选择地址的值：{{addressValue}}</p>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        selectValue: '',
        selectAddress: '',
        addressValue: 'null'
      };
    },
    methods: {
      changeValue(val) {
        this.addressValue = val;
        console.log(val);
      }
    }
  };
</script>
<style scoped>
  .select {}
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
  <iframe src="https://zxhuan.github.io/eg/#/select" class="iframe"></iframe>
</div>

## zx-select Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
place | placeholder| string| - |空
value| 值| string,number|-|必填
rules|规则校验|Object|-|案例{ required: true,  msg: '请选择地址' }

## zx-option Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
value| 值| string,number|-|必填
diabled| 是否默认禁止| boolean|true,false|false

## zx-select Events
事件名称 | 说明|回调参数
---|---|---
change | change事件|回调event