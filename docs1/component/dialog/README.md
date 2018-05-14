# dialog
```html
<template>
  <div class="dialog">
    <h2>toast</h2>
    <div class="flex">
      <zx-button @click="toastFn('bottom')" type='primary'>toast['bottom']</zx-button>
      <zx-button @click="toastFn('top')" type='primary'>toast['top']</zx-button>
      <zx-button @click="toastFn('center')" type='primary'>toast['center']</zx-button>
      <zx-button @click="toastFn('top',5000)" type='success'>5s后移除</zx-button>
      <zx-button @click="removeFn" type='warning'>弹出，但不移除</zx-button>
    </div>
    <h2>alert</h2>
    <div class="flex">
      <zx-button @click="alertFn"  type='success'>alert</zx-button>
    </div>
    <h2>confirm</h2>
    <div class="flex">
      <zx-button @click="confirmFn" type='danger'>confirm</zx-button>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        moveBool: false
      };
    },
    methods: {
      removeFn() {
        this.$dialog.toast({
          msg: '弹出，但不移除',
          remove: false // 默认为true【移除】，false[不移除]
        });
      },
      toastFn(direction, duration) {
        this.$dialog.toast({
          msg: direction,
          position: direction,
          time: duration ? duration : '', // 时间间隔
          onOk: () => {
            console.log('hello world!');
          }
        });
      },
      alertFn() {
        this.$dialog.alert({
          msg: '弹层信息',
          onOk: () => {
            console.log('alertFn callback');
          }
        });
      },
      confirmFn() {
        this.$dialog.Confirm({
          title: '温馨提示',
          msg: '此操作将删除该条数据，是否继续',
          onOk: () => {
            this.$dialog.toast({
              msg: '删除成功'
            });
          },
          cancel: () => {
            this.$dialog.toast({
              msg: '取消删除'
            });
          }
        });
      }
    },
    created() {
      this.$store.dispatch('setTtile', 'dialog');
    }
  };
</script>
<style scoped>
  .dialog{
    padding: 10px;
  }
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
  <iframe src="https://zxhuan.github.io/eg/#/dialog" class="iframe"></iframe>
</div>
