## radio
```html
<template>
  <div class="radio">
    <zx-form-group title="radio选项">
      <span slot="label-text">当前选中的值:{{values}}</span>
      <zx-radio-group v-model="values" ref="values" :rules="rules.radio">
        <zx-radio-item value="value1">value1</zx-radio-item>
        <zx-radio-item value="value2" disabled>value2</zx-radio-item>
        <zx-radio-item value="value3">value3</zx-radio-item>
        <zx-radio-item value="value4">value4</zx-radio-item>
        <zx-radio-item value="value5">value5</zx-radio-item>
      </zx-radio-group>
    </zx-form-group>
    <div class="flex">
      <zx-button @click="submitFn" type="primary">提交</zx-button>
    </div>
    <zx-form-group title="radio选项">
      <span slot="label-text">当前选中的值:{{values1}}</span>
      <zx-radio-group v-model="values1" flex @change="changeValue(values1)">
        <zx-radio-item value="选项1">选项1</zx-radio-item>
        <zx-radio-item value="选项2">选项2</zx-radio-item>
        <zx-radio-item value="选项3">选项3</zx-radio-item>
        <zx-radio-item value="选项4">选项4</zx-radio-item>
        <zx-radio-item value="选项5">选项5</zx-radio-item>
        <zx-radio-item value="选项6">选项6</zx-radio-item>
      </zx-radio-group>
    </zx-form-group>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        values: '',
        values1: '选项1',
        rules: {
          radio: { required: true, msg: '请选中一个值' }
        }
      };
    },
    methods: {
      changeValue(value) {
        console.log(value);
      },
      // 代码提交
      submitFn() {
        if (!this.$refs['values'].valid) {
          this.$dialog.toast({
            msg: this.$refs['values'].msg,
            position: 'top'
          });
          return false;
        }
        console.log(this.values);
      },
      getValue(val) {
        console.log(val);
      }
    }
  };
</script>
<style scoped>
  .flex {
    margin-bottom: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-bottom: 10px;
  }

  .flex .zx-button {
    margin-bottom: 10px;
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
  <iframe src="https://zxhuan.github.io/eg/#/radio" class="iframe"></iframe>
</div>

## zx-radio-group Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
place | placeholder| string| - |空
value| 值| string,number|-|必填
rules|规则校验|Object|-|案例{ required: true,  msg: '请选择性别' }
flex| radio排列方式| boolean|true,false|false

## zx-radio-item Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
value| 值| string,number|-|必填
diabled| 是否默认禁止| boolean|true,false|false

## zx-radio-group Events
事件名称 | 说明|回调参数
---|---|---
change | change事件|回调event