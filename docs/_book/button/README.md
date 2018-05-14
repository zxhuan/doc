# button
```html
<template>
  <div class="button">
    <zx-button type='primary'>primary</zx-button>
    <zx-button type='success'>success</zx-button>
    <zx-button type='info'>info</zx-button>
    <zx-button type='warning'>warning</zx-button>
    <zx-button type='danger'>danger</zx-button>
    <zx-button type='primary' size='min'>button min</zx-button>
    <zx-button type='primary' size='large'>{{largeButton}}</zx-button>
    <zx-button type='primary' @click="clickFn">click button</zx-button>
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
    }
  };
</script>
<style scoped>
  .button {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
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