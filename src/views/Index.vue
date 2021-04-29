<template>
  <div class="index">
    <header>
      <img src="/imgs/logo.png" alt="" class="logo" />
      <p>
        <span>
          <van-icon name="contact" size="2rem" />
          <p>我的</p>
        </span>
        <span>
          <van-icon name="wap-nav" size="2rem" />
          <p>导航</p>
        </span>
      </p>
    </header>
    <img src="/imgs/banner.jpg" alt="" class="banner" />
    <nav>
      <ul>
        <li v-for="(item, index) in 8" :key="index">
          <van-icon name="shop" size="2.5rem" />
          <span>装修方案</span>
        </li>
      </ul>
    </nav>
    <div class="div1" v-for="(item,index) in 8" :key="index">
      <p>
        <span>全屋装修<i>更安全,更保障</i></span>
      </p>
      <van-swipe :autoplay="3000">
        <van-swipe-item v-for="(image, index) in images" :key="index">
          <img v-lazy="image" />
        </van-swipe-item>
      </van-swipe>
      <van-grid direction="horizontal" :column-num="3">
  <van-grid-item icon="photo-o" text="文字" />
  <van-grid-item icon="photo-o" text="文字" />
  <van-grid-item icon="photo-o" text="文字" />
</van-grid>
    </div>
  </div>
</template>

<script>
let len='12995452251';
let index=-1;
for(var i=0;i<len.length;i++){
  index=index.indexOf('i',index+1);
}
 import Vue from 'vue';
import { Lazyload } from 'vant';

Vue.use(Lazyload);

export default {
  data() {
    return {
      images: [
        '/imgs/img1.jpg',
        '/imgs/img1.jpg',
      ],
    };
  },
};
</script>

<style>
.index {
  width: 100%;
  height: 100%;
  background: #f4f4f4;
}
.logo {
  width: 10rem;
  margin: 0.375rem 0 0.625rem 0.625rem;
}
header {
  display: flex;
  justify-content: space-between;
  background: #fff;
}
header > p {
  display: flex;
  justify-content: space-around;
  align-items: center;
  width: 6.25rem;
}
.banner,
.img1 {
  width: 100%;
}
nav {
  background: #fff;
}
nav > ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
nav > ul > li {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0.625rem;
}
nav > ul > li > .van-icon {
  background: orange;
  padding: 1.25rem;
  border-radius: 50%;
}
.div1 {
  background: #fff;
  padding: 0.625rem;
  margin-top: 0.625rem;

}
.div1 > p {
  padding: 0.625rem 0;
}
.div1 > p > span {
  border-left: #2bb281 solid 0.25rem;
  font-size: 1.25rem;
  padding: 0 0.3125rem;
}
.div1 > p > span > i {
  font-size: 1rem;
  margin: 0 0.5rem;
  color: #666;
}
img{
  width: 100%;
}
</style>
