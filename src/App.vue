<template>
  <!-- <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/> -->
  <div id="container">
    <div id="navbar">
      <div id="top">
        <div id="logo">
          <h1>NARCISSUS</h1>
        </div>
        <div id="bars">
          <!-- <div id="login"></div> -->
        </div>
      </div>
      <div id="bottom">
        <ul id="menu">
          <li><a href="">SWIM</a></li>
          <li><a href="">BESTSELLERS</a></li>
          <li><a href="">LINGERIE</a></li>
          <li><a href="">SETS</a></li>
          <li><a href="">PROVOCATIVE</a></li>
          <li><a href="">NIGHTWEAR</a></li>
          <li><a href="">HOSIERY</a></li>
          <li><a href="">CLOTHING</a></li>
          <li><a href="">GIFTS</a></li>
          <li><a href="">OUTLET</a></li>
        </ul>
      </div>
    </div>
    <div class="section-one">
      <div id="video-container">
        <video id="my-video" autoplay loop muted>
          <source src="./Narcissus.mp4" type="video/mp4">
          <!-- Farklı video formatları için buraya gerekli kaynakları ekleyebilirsiniz -->
        </video>
      </div>
    </div>
  </div>
</template>

<style lang="scss">

@font-face {
  font-family: 'narcissus'; /* Fontunuzun ismi */
  src: url('lfont.otf') format('opentype'); /* Font dosyasının URL'si ve formatı */
}
@font-face {
  font-family: 'menu'; /* Fontunuzun ismi */
  src: url('afont.ttf') format('opentype'); /* Font dosyasının URL'si ve formatı */
}

#container{
  overflow-x: hidden;
}

#video-container {
  position: relative;
  width: 100%;
  max-width: 100%;
  height: auto;
  z-index: -1; /* Videoyu diğer öğelerin arka planına yerleştirir */
}

#my-video {
  width: 100%;
}

#navbar {
  width: 100%;
  height: 130px;
  max-height: 130px;
  border: 1px solid rgb(219, 220, 207);
  display: flex;
  flex-direction: column;
  overflow: hidden;
  background-color: rgb(255, 255, 255);
  position: relative; /* Navbar'ın pozisyonunu belirtir */
  z-index: 1; /* Navbar'ı videoya göre üstte tutar */
}

#top {
  flex: 1;
  display: flex;
  justify-content: center; /* Yatayda ortalamak için */
  align-items: center; /* Dikeyde ortalamak için */
}

#top h1{
  font-family: narcissus;
  font-weight: 500;
  font-size: 36px;
  letter-spacing: 0.090em;
  margin-bottom: -2px;
}

#bottom {
  flex: 1;
  //overflow-y: auto; /* Gerekirse, menü içeriği çok fazla ise dikey kaydırma çubuğu ekler */
  display: flex;
  justify-content: center; /* Yatayda ortalamak için */
  align-items: center; /* Dikeyde ortalamak için */
}

#menu {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
  flex-wrap: nowrap; /* Menü öğelerinin yan yana olmasını sağlar */
  overflow-x: auto; /* Gerekirse, menü içeriği çok fazla ise yatay kaydırma çubuğu ekler */
}

#menu li {
  padding: 10px 20px; /* Örnek dolgu (padding) ayarı */
  white-space: nowrap; /* Yazıların bir satırda kalmasını sağlar */
  font-family: menu;
  font-weight: 600;
  letter-spacing: 0.1em;
  font-size: 15px;
}

#menu li a{
  text-decoration: none;
  color:black;
}

body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif; /* Örnek bir yazı tipi ayarı */
}


</style>
