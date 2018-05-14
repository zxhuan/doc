# popup
```html
<template>
  <div class="popup">
    <zx-button @click="popupFn('left','40%','40%')">左边弹出</zx-button>
    <hr>
    <zx-button @click="popupFn('right')">右边弹出</zx-button>
    <hr>
    <zx-button @click="popupFn('bottom')">底部弹出</zx-button>
    <hr>
    <zx-button @click="popupFn('top')">顶部弹出</zx-button>
    <zx-popup v-model="showBool" :position="direction" :width="w" :height="h" @close="closeMask">
      <zx-button type="warning" @click="showBool=!showBool" style="margin:10px;">点我关闭图层</zx-button>
    </zx-popup>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        showBool: false,
        direction: 'right',
        h: '60%',
        w: '60%'
      };
    },
    methods: {
      popupFn(direction, h, w) {
        this.showBool = true;
        this.direction = direction;
        this.h = h ? h : '60%';
        this.w = w ? w : '60%';
      },
      closeMask() {
        console.log('关闭图层');
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
  <iframe src="https://zxhuan.github.io/eg/#/popup" class="iframe"></iframe>
</div>