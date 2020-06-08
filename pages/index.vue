<template>
  <div class="container">
    <h1><img src="../components/logo.png" alt="바나프레소 로고" class="logo"></h1>
    <div class="link_box">
      <span class="here">Here &#129047;</span>
      <ul class="links">
        <li><nuxt-link to="/order">주문</nuxt-link></li>
        <li><nuxt-link to="/member">멤버십</nuxt-link></li>
        <li><nuxt-link to="/mypage">내 정보</nuxt-link></li>
      </ul>
    </div>      
  </div>
</template>

<script>
  export default {
    head: {
      title: '모바일 바나프레소',
      meta: [
        { hid: 'description', name: 'description', content: '바나프레소 모바일 결제' }
      ],
      noscript: [
        { innerHTML: 'Body No Scripts', body: true }
      ]
    }
  }
</script>

<style lang="scss" scoped>
$primaryColor: #f66b91;
ul{margin: 0;padding: 0;}
li{list-style: none;}
a{color: #1a1a1a;}
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap');

.container{
  display: flex;
  flex-direction: column;
  width: 575px;
  background: url(../components/icetea.jpg) center top no-repeat;
  background-size: cover;
  height: 100vh;
  font-family: 'Noto Sans KR', sans-serif;
  h1{
    text-align: center;
    margin-top: 28px;
    .logo{
      width: 22%;
    }
  }
}

.link_box {
  justify-content: center;
  margin-top: auto;
  padding: 40px 0;
  .here{
    display: block;
    text-align: center;
    font-weight: bold;
    color: #999;
    background: url(../components/rabbit.png) 62% top no-repeat;
    background-size: contain;
    padding: 10px 0;
    margin: 10px 0;
    animation-name: click;
    animation-duration: 1.6s;
    animation-iteration-count: infinite;
    transition-timing-function: ease;
  }
  @keyframes click {
    0%{color: #999;margin-bottom: 10px;}
    50%{color: $primaryColor;margin-bottom: 15px;}
    100%{color: #999;margin-bottom: 10px;}
  }
  .links{
    display: flex;
    justify-content: center;
    li{
      margin: 0 10px;
      background: #fff;
      border-radius: 50%;
      width: 60px;
      height: 60px;
      box-shadow: 2px 2px 4px 0px #ccc;
      a{
        display: flex;
        width: 100%;
        height: 100%;  
        align-items: center;
        justify-content: center;   
        color: #1a1a1a;
        font-size: 14px;
        &:hover{
          font-weight: bold;
        } 
      }
    }
  }
}

@media (max-width: 575px){
  .container{
    width: 100%;
    padding-right: 0;
    padding-left: 0;
  }
}
</style>
