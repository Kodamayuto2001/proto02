<template>
  <div class="header">
    <nav class="gnav">
      <ul class="menu">
        <li><a href="">Home</a></li>
        <li><a href="">Login</a></li>
      </ul>
    </nav>
  </div>
  
  <img alt="Vue logo" src="./assets/logo.png" class="text-logo">
  <TopPage msg=""/>
</template>

<script>
import TopPage from './components/TopPage.vue'

export default {
  name: 'App',
  components: {
    TopPage
  }
}
</script>

<style>
img.text-logo {
  margin-top: 10px;
}
body {
  padding-top: 90px; /* ヘッダーの後ろに要素が隠れないようにするため */
  background-color: #FFF;
}
.header {
  width: 100%; /* 幅いっぱいを指定 */
  height: 50px; /* 高さを50pxに指定 */
  background: #CCC; /* 背景色にグレーを指定 */
  padding: 20px 50px; /* ヘッダーに上下左右それぞれ余白を指定 */
  box-sizing: border-box; /* padding分を含んで幅を100%にするため */
  position: fixed; /* ウィンドウを基準に画面に固定 */
  top: 0; /* 上下の固定位置を上から0pxにする */
  left: 0; /* 左右の固定位置を左から0pxにする */
  display: flex; /* 中の要素を横並びにする */
  align-items: center; /* 中の要素を上下中央に並べる */
  background-color: #321E10;
}
.header .gnav .menu {
  display: flex; /* 中の要素を横並びにする */
}

.header .gnav .menu li a {
  color: #FFF;
  list-style: none; /* リストの[・]を消す */
}

.header .gnav .menu li + li {
    margin-left: 40px; /* メニューそれぞれに間隔をあけるため */
}

main {
    height: 100vw; /* スクロールの演出を見れるようにmainに高さを指定 */
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* .header .gnav .menu {
  position: relative;
  display: inline-block;
  text-decoration: none;
}
.header .gnav .menu ::after{
  position: absolute;
  bottom: -4px;
  left: 0;
  content: '';
  width: 100%;
  height: 2px;
  background: #333;
  transform: scale(0, 1);
  transform-origin: left top;
  transition: transform .3s;
}
.header .gnav .menu :hover::after {
  transform: scale(1, 1);
} */
</style>
