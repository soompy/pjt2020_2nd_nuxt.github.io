<template>
  <div class="container">
      <header id="header">
        <ul class="gnb">
          <li><nuxt-link to="/best">Best</nuxt-link></li>
          <li><nuxt-link to="/best">All</nuxt-link></li>
          <li><nuxt-link to="/best">Coffee</nuxt-link></li>
          <li><nuxt-link to="/best">Tea</nuxt-link></li>
          <li><nuxt-link to="/best">Set Menu</nuxt-link></li>
          <li><nuxt-link to="/best">Bread</nuxt-link></li>
          <li><nuxt-link to="/best">Juice</nuxt-link></li>
        </ul>
      </header>
      
      <section class="menuWrp">
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
      </section>     
      <section class="menuWrp">
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
      </section>  
      <section class="menuWrp">
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
        <div class="menu_box">  
          <nuxt-link to="/payment">
            <span class="menu_img"><img src="../components/menu_paniniset.png" alt="세트"></span>
            <p class="menu">베이컨파니니세트<span class="eng">Bacon Panini Set</span></p>
            <strong class="price">5,000~5,300원</strong>
          </nuxt-link>
        </div>
      </section> 
    </div>
  
</template>

<script>
  export default {
    head: {
      title: '메뉴선택 바나프레소',
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
a{text-decoration: none;color: #1a1a1a;}

#header{
  width: 575px;
  background: $primaryColor;
  .gnb{
    display: flex;
    li{
      flex: 1;
      text-align: center;
      a{
        display: block;
        padding: 8px 0;
        color: #fff;
        &:hover{
          font-weight: bold;
          text-decoration: none;
        }
      }
    }
  }
}

.container{
  display: block;
  width: 575px;
  height: 100vh;
  font-family: 'Noto Sans KR', sans-serif;
  .menuWrp{
    display: flex;
    width: 575px;
    .menu_box{
      display: flex;
      flex: 1;
      align-items: center;
      flex-direction: column;
      padding: 1vw;
      .menu_img{
        display: block;
        text-align: center;
      }
      .menu{
        font-size: 14px;
        margin: 10px 0;
      }
      .eng{
        display: block;
        font-size: 12px;
        color: #666;
      }
      .price{
        color: $primaryColor;
        font-size: 14px;
      }
    }
  }
}

@media (max-width: 575px){
  #header{
    overflow: scroll;
    width: 100%;
    .gnb{
      width: 140%;
      font-size: 14px;
    }
  }
  .container{
    width: 100%;
    padding-right: 0;
    padding-left: 0;
    .menuWrp{
      width: 100%;
      .menu_box{
        padding: 2vw 1vw;
        a{
          width: 100%;
          .menu_img{
            width: 80%;
            height: 80%;
            margin: auto;
            img{
              width: 100%;
            }
          }
          .menu,.price{font-size: 12px;}
        }
      }
    }
  }
}
</style>
