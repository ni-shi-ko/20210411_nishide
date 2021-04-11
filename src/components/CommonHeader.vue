<template>
  <div id="header">
    <div class="header_wrap">
      <div class="header_left">TECH</div>
      <div class="header_right">
        <ul>
         <li><a href="./index.html">ホーム</a> </li>
         <li><a href="./service.html">事業内容</a></li>
         <li><a href="./news.html">ニュース</a></li>
         <li><a href="./blog.html">社員ブログ</a></li>
         <li><a href="./company.html">会社概要</a></li>
         <li><a href="./recruit.html">採用情報</a></li>
         <li><a href="./contact.html">お問い合わせ</a></li>
        </ul>
      </div>
    </div>
 <div id="humberger" @click="humberger()" :class="{'active':isClass}">
      <span></span>
      <span></span>
      <span></span>
 </div>
    <div class="menu_content" :class="{'open':isClass}">
      <p class="menu_title">>estra inc.</p>
      <ul class="menu_contant_inner">
         <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">about</a>
        </li>
        <li>
          <a href="#">service</a>
        </li>
        <li>
          <a href="#">works</a>
        </li>
        <li>
          <a href="#">price</a>
        </li>
        <li>
          <a href="#">contact</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isClass:false
    };
  },
  methods: {
    humberger() {
      this.isClass = !this.isClass;
    }
  }
};
</script>
<style scoped>
#header {
  height: 70px;
}
.header_wrap {
  display: flex;
  justify-content: space-between;
  line-height: 70px;
  z-index: 1;
  position: fixed;
  width: 100%;
  background-color: #fff;
}
.header_left {
  margin-left: 2%;
  font-size: 25px;
  font-weight: bold;
}
.header_right ul {
  display: flex;
}
.header_right li {
  list-style: none;
  margin-right: 30px;
  font-weight: bold;
}
.header_right a {
  text-decoration: none;
  color: #000000;
}
.header_right a:hover {
  opacity: 0.8;
}
 @media screen and (max-width: 768px) {
  /* header */
  header {
    position: fixed;
    width: 100%;
  }
   .header_wrap {
    z-index: 1;
  }
  /* humberger */
  #humberger {
    width: 40px;
    height: 40px;
    position: fixed;
    cursor: pointer;
    z-index: 1;
    top: 13px;
    right: 25px;
    transition: 0.4s;
  }
  #humberger span {
    position: absolute;
    left: 2px;
    display: block;
    width: 35px;
    height: 3.5px;
    background-color: #000000;
    transition: 0.8s;
  }
  #humberger span:nth-of-type(1) {
    top: 5px;
  }
  #humberger span:nth-of-type(2) {
    top: 20px;
  }
  #humberger span:nth-of-type(3) {
    top: 35px;
  }
   .header_right {
    display: none;
  }
  .header_left {
    margin-left: 30px;
    font-size: 24px;
  }
    #hamburger.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }

  #hamburger.active span:nth-of-type(2) {
    opacity: 0;
  }
  #hamburger.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg);
  }
  .menu_content {
    display: block;
    width: calc(100% - 80px);
    height: 100%;
    text-align: center;
    transition: 0.2s;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    background: #fff;
    color: #333333;
    box-shadow: 80px 0 rgba(38, 98, 213, 0.3);
    z-index: 999;
  }
  .menu_content .menu_title {
    margin: 40px 20px;
    font-size: 2.2rem;
    color: #333333;
    text-align: left;
    font-weight: bold;
  }
  .menu_content li a {
    color: #333333;
    margin: 15px;
    padding: 5px;
    border-bottom: 0.5px solid #2662d5;
    text-decoration: none;
    display: block;
  }
  .menu_content li {
    width: 100%;
    text-align: left;
  }
  .menu_content.open {
    left: 0;
  }
 }
</style>