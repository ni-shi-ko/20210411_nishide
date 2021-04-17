<template>
  <div id="footer">
  <div class="footer_wrap">
    <div class="footer_left">
      © 2020 TECH inc.
    </div>
  <div class="footer_right">
       <ul>
      <li class="first_list"><a href="./index.html">Home</a></li>
      <li>
        <a href="./service.html">
          Service
        </a>
      </li>
      <li><a href="./news.html">News</a></li>
      <li><a href="./blog.html">Blog</a></li>
      <li><a href="./company.html">Company</a></li>
      <li><a href="./recruit.html">Recruit</a></li>
      <li class="last_list"><a href="./contact.html">Contact</a></li>
    </ul>

  </div>
  </div>
</div>
</template>

<style scoped>
  #footer {
  background-color: #222323;
  color: #fff;
  padding: 1.5% 1%;
}
.footer_wrap {
  display: flex;
  justify-content: space-around;
}
.footer_left {
  font-size: 13px;
}
.footer_right ul {
  display: flex;
}
.footer_right li {
  font-size: 13px;
  list-style: none;
  display: inline;
  list-style-type: none;
  margin-right: 10px;
  padding-left: 10px;
  border-left: 1px solid #999;
  opacity: 0.8;
}
#footer .first_list {
  border-left: none;
  padding-left: 0;
}
.footer_right a {
  color: #fff;
  text-decoration: none;
}
.footer_right a:hover {
  opacity: 0.8;
}
@media screen and (max-width: 768px) {
    /* footer */
  #footer {
    padding:15px 0 ;
  }
  .footer_wrap {
    display: inline;
  }
  .footer_left {
    text-align: center;
    font-size: 12.5px;
    margin-top: 10px;
  }
  .footer_right ul {
   display: flex;
   flex-direction: column;
   text-align: center;
  }
.footer_right li {
  border: none;
  padding: 0;
  margin-bottom: 16px;
  font-size: 12.5px;
}
.first_list {
  margin-top: 20px;
}
.last_list {
  margin-bottom: 10px;
}

}
</style>
