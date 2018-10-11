## icon
``` html
<template>
  <div>
    <ul class="icon-list">
      <li class="icon-item" v-for="(item,key) of iconList" :key="key">
        <zx-icon :name='item.name' :scale="item.scale?item.scale:''" :color="item.color?item.color:''"></zx-icon>
        <p>{{item.name}}</p>
      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        iconList: [{ name: 'app-o', scale: '2.5', color: '#019dfa' }, { name: 'air-drop-o', scale: '2.5', color: '#019dfa' }, { name: 'add-r-o', scale: '2.5', color: '#019dfa' }, { name: 'app-o', scale: '2.5', color: '#019dfa' }, { name: 'air-drop-o', scale: '1.5', color: '#000' }, { name: 'add-r-o', scale: '1.5', color: '#000' }, { name: 'like', scale: '1.5', color: '#f00' }, { name: 'likefill', scale: '1.5', color: '#f00' }, { name: 'roundcheck', scale: '1.5', color: '#000' }, { name: 'arrow-right', scale: '1.5', color: '#000' }, { name: 'arrow-left', scale: '1.5', color: '#000' }, { name: 'arrow-down', scale: '1.5', color: '#000' }, { name: 'word-o', scale: '1.5', color: '#000' }, { name: 'wave-o', scale: '1.5', color: '#000' }, { name: 'volume-o', scale: '1.5', color: '#000' }, { name: 'warehouse-o', scale: '1.5', color: '#000' }, { name: 'volumeopen-o', scale: '1.5', color: '#000' }, { name: 'wallet-o', scale: '1.5', color: '#000' }, { name: 'visible-o', scale: '1.5', color: '#000' }, { name: 'vertical-retraction-', scale: '1.5', color: '#000' }, { name: 'view-list-o', scale: '1.5', color: '#000' }, { name: 'user-r-o', scale: '1.5', color: '#000' }, { name: 'vedio-o', scale: '1.5', color: '#000' }, { name: 'unseen-o', scale: '1.5', color: '#000' }, { name: 'unseen-o', scale: '1.5', color: '#000' }, { name: 'user-o', scale: '1.5', color: '#000' }, { name: 'unsatisfy-o', scale: '1.5', color: '#000' }, { name: 'unlock-o', scale: '1.5', color: '#000' }, { name: 'trend-chart-o', scale: '1.5', color: '#000' }, { name: 'transfer-station-o', scale: '1.5', color: '#000' }, { name: 'top-o', scale: '1.5', color: '#000' }, { name: 'time-o', scale: '1.5', color: '#000' }, { name: 'text-o', scale: '1.5', color: '#000' }, { name: 'template-o', scale: '1.5', color: '#000' }, { name: 'quality-o', scale: '1.5', color: '#000' }, { name: 'diamond-o', scale: '1.5', color: '#000' }, { name: 'cainixihuan', scale: '1.5', color: '#000' }, { name: 'tishishuoming', scale: '1.5', color: '#000' }, { name: 'shouhuodizhiyebianji', scale: '1.5', color: '#000' }, { name: 'text-o', scale: '1.5', color: '#000' }, { name: 'changyonggoupiaorenshanchu', scale: '1.5', color: '#000' }, { name: 'pingjia', scale: '1.5', color: '#000' }, { name: 'daishouhuo', scale: '1.5', color: '#000' }, { name: 'daifukuan', scale: '1.5', color: '#000' }, { name: 'daifukuan', scale: '1.5', color: '#000' }, { name: 'dizhiguanli', scale: '1.5', color: '#000' }, { name: 'guanyanren', scale: '1.5', color: '#000' }, { name: 'yigouxuan', scale: '1.5', color: '#000' }, { name: 'sousuo', scale: '1.5', color: '#000' }, { name: 'faxian', scale: '1.5', color: '#000' }, { name: 'xiaoxi', scale: '1.5', color: '#000' }, { name: 'xiaoxi', scale: '1.5', color: '#000' }, { name: 'fenlei', scale: '1.5', color: '#000' }, { name: 'shouye', scale: '1.5', color: '#000' }, { name: 'saoyisao', scale: '1.5', color: '#000' }, { name: 'shoucang', scale: '1.5', color: '#000' }, { name: 'zanting', scale: '1.5', color: '#000' }, { name: 'shenfenzheng', scale: '1.5', color: '#000' }, { name: 'kefu', scale: '1.5', color: '#000' }, { name: 'guanbi', scale: '1.5', color: '#000' }, { name: 'fanhui', scale: '1.5', color: '#000' }, { name: 'fanhui', scale: '1.5', color: '#000' }, { name: 'fenxiang', scale: '1.5', color: '#000' }]
      };
    }
  };
</script>
<style scoped>
  .icon-list {
    padding: 0;
    margin: 0;
  }

  .icon-list {
    position: relative;
    display: flex;
    flex-wrap: wrap;
  }

  .icon-item {
    width: 25%;
    /* flex: 1; */
    display: flex;
    flex-direction: column;
  }

  p {
    font-size: 12px;
  }
</style>
```
## zx-icon Attributes
参数 | 说明 | 类型 |可选值 |默认值
---|---|---|---|---
name | icon名称| string| - |必填
scale | 图标比例| number| - |非必填
color | 图标颜色| string| - |非必填
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
  <iframe src="https://zxhuan.github.io/eg/#/icon" class="iframe"></iframe>
</div>