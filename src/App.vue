<template>
<div id="app">
  <CommonHeader></CommonHeader>
    <div id="top">
    <div class="top_wrap">
    <div class="top_message">
    <h1>最新のテクノロジーで社会課題を解決</h1>
    <p>Solving social issues with the latest technology</p>
    </div>
    </div>
  </div>
    <div class="tech_message">
      <h2>株式会社TECHの想い</h2>
      <p>
        あらゆる産業において、新たなデジタル技術を使ってこれまでにないビジネスモデルを展開する新規参入者が登場し、ゲームチェンジが起ころうとしています。こうした中で、各企業は、競争力維持・強化のために、DXを迅速に進めていくことが求められています。しかし、DXにおいて投資コストは非常にかかります。株式会社TECHでは独自のオペレーションと人材教育により、他社よりも価格を抑えた開発を行います。
      </p>
   </div>
    <div id="service">
      <div class="service_title">サービス</div>
      <div class="service_wrap">
       <div class="service_container">
         <img src="./assets/img/service1.png" alt="">
        
         <h3>IT人材育成事業</h3>
         <p>これまでに培った教育手法を生かして、短期間で即戦力のIT人材を育成します。</p>
        </div>
        <div class="service_container">
          <img src="./assets/img/service2.png" alt="" >
          <h3>コーチング事業</h3>
          <p>目標達成を最短で実現するために、プロのコーチによるマンツーマンのサポートを実施します。</p>
        </div>
          <div class="service_container">
            <img src="./assets/img/service3.png" alt="">
            <h3>ITコンサル事業</h3>
            <p>経営戦略にIT戦略を策定し、システム開発の提案やシステムの最適化を通じて、企業の経営をサポートします。</p>
          </div>
            <div class="service_container">
              <img src="./assets/img/service4.png" alt="">
              <h3>デジタルトランスフォーメーション事業</h3>
              <p>人々の生活をよりよいものに変革するために様々なデジタル技術を活用し、革新的なソリューションやサービスを生み出します。</p>
            </div>
       </div>

        <div class="service_btn">
          <button class="service_button" type="submit">
            <a href="./service.html">サービス一覧をみる</a>
          </button>
        </div>
    </div>
     <!-- news -->
    <div id="news">
      <div class="news_title">
      <div class="news_left">ニュース</div>
      <div class="news_right">
        <div class="news_btn">
          <button class="news_button" type="submit"><a href="./news.html"></a>ニュース一覧をみる</button>
        </div>
      </div>
      </div>
      <div class="news_list">
      <div class="news_message" v-for="(data, index) in Newses" :key="index">
       <a href=""></a>
       <p>{{data.date}}</p>
       <h3>{{data.sentence}}</h3>
      </div>
      </div>
    </div>
      <!-- blog -->
    <div id="blog">
      <div class="blog_title">社員ブログ</div>
      <div class="blog_wrap">
        <div class="blog_container" v-for="(data, index) in Blogs" :key="index">
          <img :src="data.img" alt/>
          <p>{{data.date}}</p>
          <h3><a href="">{{data.sentence}}</a></h3>
        </div>
      </div>
      <div class="service_btn">
        <button class="service_button blog_button" type="submit">
          <a href="./service.html">サービス一覧をみる</a>
          </button>
        </div>
      </div>
       <!-- company -->
  <div id="company">
    <div class="company_wrap">
    <a href="./company.html" class="company_text">
    <p>会社概要</p>
    </a>
    <a href="./recruit.html" class="recruit_text">
     <p>採用情報</p>
   </a>
    </div>
  </div>
  <!-- contact -->
  <div id="contact">
    <div class="contact_wrap">
    <div class="contact_message">
      <h2>お問い合わせ</h2>
     <p>お仕事のご依頼や採用に関してはお問い合わせにて承っております。</p>
   </div>
   </div>
   <div class="service_btn contact_btn">
      <button class="service_button contact_button" type="submit">
       <a href="./contact.html">お問い合わせ</a>
      </button>
    </div>
  </div>

  <CommonFooter></CommonFooter>
</div>
</template>

<script>
import CommonHeader from "./components/CommonHeader.vue";
import CommonFooter from "./components/CommonFooter.vue";
export default {
  data() {
    return{
      Blogs:[
        {
          img: require("./assets/img/blog.png"),
          date:"2019/07/17",
          sentence:"会社を創業した理由"
        },
        {
          img: require("./assets/img/blog.png"),
          date:"2019/11/11",
          sentence:"ITエンジニアを育成育成する最強メソッド"
        },
        {
          img: require("./assets/img/blog.png"),
          date:"2020/08/01",
          sentence:"コーチングによるモチベーション向上理論"
        }
      ],
      Newses:[
        {
          a:"#",
          date:"2019/07/17",
          sentence:"会社を創業しました。"
        },
        {
          a:"#",
          date:"2020/04/01",
          sentence:"資金調達を行いました。"
        },
        {
          a:"#",
          date:"2020/10/01",
          sentence:"東京新聞に掲載されました。"
        }
      ]
    };
  },
  components: {
    CommonHeader,
    CommonFooter
  }
};
</script>

<style>
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
  margin:0;
  padding:0;
  border:0;
  outline:0;
  font-size:100%;
  vertical-align:baseline;
  background:transparent;
}

body {
  line-height:1;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
  display:block;
}

nav ul {
  list-style:none;
}

blockquote, q {
  quotes:none;
}

blockquote:before, blockquote:after,
q:before, q:after {
  content:'';
  content:none;
}

a {
  margin:0;
  padding:0;
  font-size:100%;
  vertical-align:baseline;
  background:transparent;
}

/* change colours to suit your needs */
ins {
  background-color:#ff9;
  color:#000;
  text-decoration:none;
}

/* change colours to suit your needs */
mark {
  background-color:#ff9;
  color:#000;
  font-style:italic;
  font-weight:bold;
}

del {
  text-decoration: line-through;
}

abbr[title], dfn[title] {
  border-bottom:1px dotted;
  cursor:help;
}

table {
  border-collapse:collapse;
  border-spacing:0;
}

/* change border colour to suit your needs */
hr {
  display:block;
  height:1px;
  border:0;
  border-top:1px solid #cccccc;
  margin:1em 0;
  padding:0;
}

input, select {
  vertical-align:middle;
}
/* top */
#top {
  background-image: url("./assets/img/mv.png");
  background-size: cover;
  background-position: center;
  background-position: center;
  height: 80vh;
  position: relative;
}
.top_wrap {
  position: absolute;
  top: 45%;
  left: 25%;
}
.top_message h1 {
  font-size: 50px;
  color: #ffffff;
  margin-bottom: 20px;
}
.top_message p {
  font-weight: bold;
  font-size: 18px;
  color: #ffffff;
  text-align: center;
}
/* tech */
.tech_message {
  background-color: #222323;
  color: #ffffff;
  padding: 5% 18%;
  box-sizing: border-box;
}
.tech_message h2 {
  font-size: 30px;
  margin-bottom: 30px;
}
.tech_message p {
  line-height: 1.5;
}
/* service */
.service_title {
  text-align: center;
  font-size: 30px;
  font-weight: bold;
  margin: 80px 0 30px 0;
}
.service_wrap {
  width: 70%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding-right: 30px; 
}
.service_container {
  width: 45%;
  margin-left: 25px;
  box-sizing: border-box;
}
.service_container img {
  display: block;
  width: 100%;
}
.service_container h3 {
  margin: 7px 0;
}
.service_container p {
  width: 100%;
  line-height: 1.5;
  margin-bottom: 10px;
}
.service_btn {
  text-align: center;
  margin-bottom: 30px;
}
.service_button {
  margin: 30px 0 50px 0;
  background-color: #cd0323;
  padding: 13px 85px;
  border: none;
}
.service_button a {
  color: #ffffff;
  font-weight: bold;
  font-size: 15px;
  line-height: 1.5;
  text-decoration: none;
}
.service_button:hover {
  opacity: 0.8;
}
/* news */
#news {
  background-color: #222323;
  padding: 5% 15%;
}.news_title {
  display: flex;
  justify-content: space-between;
  line-height: 1.5;
}
.news_left {
  color: #fff;
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 30px;
}
.news_button {
  border: none;
  background-color: #cd0323;
  color: #fff;
  padding: 7px 20px;
  font-weight: bold;
}
.news_button:hover {
  background-color: rgba(154, 24, 37, 1.0);
}
.news_message {
  background-color: #fff;
  width: 100%;
  margin-bottom: 10px;
  padding: 23px 0px 23px 0;
  box-sizing: border-box;
  display: flex;
  line-height: 1.5;

}
.news_message p {
  margin-left: 25px;
}
.news_message h3 {
  margin-left: 10px;
}
.news_message:hover {
  background-color: rgba(188, 188, 188, 1.0);
}

/* blog */
.blog_title {
  text-align: center;
  font-size: 30px;
  font-weight: bold;
  margin: 80px 0 30px 0;
}
.blog_wrap {
  display: flex;
  justify-content: space-around;
  width: 65%;
  margin: 0 auto;
}
.blog_container {
  width: 33%;
  margin-left: 20px;
}
.blog_container img {
  width: 100%;
  display: block;
}
.blog_container img:hover {
  opacity: 0.8;
}
.blog_container h3 {
  margin-bottom: 8px;
}
.blog_container p {
  width: 100%;
  margin: 10px 0;
}
 .blog_container a {
  text-decoration: none;
  color: #000000; 
} 
.blog_container a:hover {
  opacity: 0.8;
}
/* company */
#company {
  margin-bottom: 5%;
}
.company_wrap {
  display: flex;
}
.company_text {
  background-color: #cd0323;
  color: #fff;
  font-size: 20px;
  font-weight: bold;
  width: 50%;
  text-align: center;
  padding: 6.5% 0;
  text-decoration: none;
}
.recruit_text {
  background-color: #222323;
  color: #fff;
  font-size: 20px;
  font-weight: bold;
  width: 50%;
  text-align: center;
  padding: 6.5% 0;
  text-decoration: none;
}
.company_text:hover,
.recruit_text:hover {
  opacity: 0.8;
}
/* contact */
#contact {
  background-color: #f5f6f9;
  padding: 5% 0 2% 0;
}
.contact_wrap {
  display: flex;
  justify-content: center;
}
.contact_message {
  text-align: center;
  line-height: 2;
}
.contact_message h2 {
  font-size: 30px;
}
.contact_message p {
  margin-bottom: 10px;
}
.contact_btn {
  margin: 0;
}
.contact_button {
  padding: 13px 90px;
}
 @media screen and (max-width: 768px) {
     /* top */
  #top {
    display: flex;
    justify-content: center;
    align-items: center;
    line-height: 1.5;
    height: 70vh;
    padding-top: 70px;
 }
 .top_wrap {
   position: static;
   width: 80%;
   margin: 0 auto;
 }
 .top_message {
   text-align: center;
   line-height: 1.7;
   margin-bottom: 30px;
 }
 .top_message h1 {
   margin-bottom: 0px;
 }
 .tech_message {
   padding: 75px 30px;
 }
 .tech_message h1 {
   text-align: center;
 }
 /* service */
 .service_wrap {
   width: 100%;
   padding-right: 0;
 }
 .service_container {
   width: 100%;
   margin-right: 25px;
 }
 .service_container p {
   margin-bottom: 30px;
 }
 .service_container h3 {
   font-size: 20px;
 }
 .service_button {
   margin: 10px 0 50px 0;
 }
 /* news */
  #news {
    padding: 90px 30px;
  }
  .news_title {
    line-height: 1.0;
  }
  .news_message {
    padding: 13px;
  }
  .news_message {
    box-sizing: border-box;
  }
  .news_message h3 {
    font-size: 14px;
    line-height: 1.0;
  }
  .news_message p {
    font-size: 14px;
    line-height: 1.0;
    margin: 0;
  }
  /* blog */
  .blog_wrap {
    width: 100%;
    flex-wrap: wrap;
  }
  .blog_container {
    width: 90%;
    margin: 0 30px 0 30px;
  }
  .blog_container h3 {
    font-size: 18px;
  }
  .blog_button {
    margin-top: 40px;
  }
  /* company */
  #company {
    margin-bottom: 80px;
  }
  .company_text,
  .recruit_text {
    padding: 110px 0;
  }
  .company_text p,
  .recruit_text p {
    font-size: 25px;
  }
  /* contact */
  #contact {
    padding: 70px 25px 40px;
  }
  .contact_button {
    padding: 13px 100px;
  }
  .contact_message p {
    margin-bottom: 25px;
    line-height: 1.4;
  }
   .service_btn {
    margin: 0;
  }
  .service_button {
    margin: 20px 0 30px 0;
  }

 }
</style>

