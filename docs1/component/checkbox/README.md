## checkbox
```html
<template>
    <div class="checkbox">
        <zx-form-group title="checkox选项">
            <span slot="label-text">当前选中的值:{{value}}</span>
            <zx-checkbox-group v-model='value' ref='value' :rules="rules.checkbox" flex >
                <zx-checkbox-item value="选项卡一">选项卡一</zx-checkbox-item>
                <zx-checkbox-item value="选项卡二" disabled>选项卡二</zx-checkbox-item>
                <zx-checkbox-item value="选项卡三" disabled>选项卡三</zx-checkbox-item>
                <zx-checkbox-item value="选项卡四">选项卡四</zx-checkbox-item>
                <zx-checkbox-item value="选项卡五">选项卡五</zx-checkbox-item>
            </zx-checkbox-group>
        </zx-form-group>
        <div class="flex">
            <zx-button @click="submitFn" type="primary">提交</zx-button>
        </div>
        <zx-form-group title="checkox选项">
            <span slot="label-text">当前选中的值:{{values}}</span>
            <zx-checkbox-group v-model='values' @change="changeValue(values)">
                <zx-checkbox-item value="value1">value1</zx-checkbox-item>
                <zx-checkbox-item value="value2">value2</zx-checkbox-item>
                <zx-checkbox-item value="value3">value3</zx-checkbox-item>
            </zx-checkbox-group>
        </zx-form-group>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                value: ['选项卡三'],
                values: [],
                rules: {
                    checkbox: { required: true, msg: '请选中一个值' }
                }
            };
        },
        methods: {
            changeValue(value) {
                console.log(value);
            },
            // 代码提交
            submitFn() {
                if (!this.$refs['value'].valid) {
                    this.$dialog.toast({
                        msg: this.$refs['value'].msg,
                        position: 'top'
                    });
                    return false;
                }
                console.log(this.value);
            }
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
  <iframe src="https://zxhuan.github.io/eg/#/checkbox" class="iframe"></iframe>
</div>

## zx-checkbox-group Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
place | placeholder| string| - |空
value| 值| string,number|-|必填
rules|规则校验|Object|-|案例{ required: true,  msg: '请选择性别' }
flex| radio排列方式| boolean|true,false|false

## zx-checkbox-item Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
value| 值| string,number|-|必填
diabled| 是否默认禁止| boolean|true,false|false

## zx-checkbox-group Events
事件名称 | 说明|回调参数
---|---|---
change | change事件|回调event