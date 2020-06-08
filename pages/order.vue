<template>
  <div class="container">
    <div class="inner">
      <h2>어디서 드시겠습니까?</h2>
      <p>환경보호에 동참해주세요.</p>
       
      <div class="order_box">
        <nuxt-link to="/best">
            <strong>테이크아웃<em>자원재활용법에 따라 매장 내 일회용 컵(플라스틱 컵) 사용이 금지되어 있습니다.</em></strong>
            <span>&#10157;</span>
        </nuxt-link>
        <nuxt-link to="/best">
            <strong>매장 &#x002B; 테이크<em>종이컵</em></strong>
            <span>&#10157;</span>
        </nuxt-link>
        <nuxt-link to="/best">
            <strong>매장<em>다회용컵</em></strong>
            <span>&#10157;</span>
        </nuxt-link>
        <nuxt-link to="/best">
            <strong>배달주문</strong>
            <span>&#10157;</span>
        </nuxt-link>
      </div>
    </div>
    <div class="popup">
      <span class="dim">-</span>
      <div class="popup_box">
          <h3>알림</h3>
          <p>현재 고객님의 위치가 매장과 <br> 300m이상 떨어져 있습니다. <br><br>고객님의 픽업이 늦어지면 메뉴가
          녹거나 식을 수 있으니 가급적 매장 가까이에서 <br> 주문하시길 권장합니다.</p>
          <div class="btn_box">
              <nuxt-link to="/">닫기</nuxt-link>
              <nuxt-link to="/best" class="go">주문하기</nuxt-link>
          </div>
      </div>
    </div>
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
// .container{min-height: auto !important;}
ul{margin: 0;padding: 0;}
li{list-style: none;}
a{color: #1a1a1a;}
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap');

.container {
    position: relative;
    display: flex;
    background: $primaryColor;
    width: 575px;
    height: 100vh;
    font-family: 'Noto Sans KR', sans-serif;
    .inner{
        width: 96%;
        margin: auto;
    }
    h2{
        text-align: center;
        font-size: 24px;
    }
    p{
        font-size: 16px;
        text-align: center;
    }
}

.order_box{
    a{
        display: flex;
        align-items: center;
        background: #fff;
        box-shadow: 1px 1px 1px 0px #ccc;
        margin: 12px 0;
        text-align: left;
        padding: 14px;
        border-radius: 10px;
        em{
            display: block;
            font-style: inherit;
            font-size: 12px;
            font-weight: normal;
        }
        span{
            display: flex;
            align-items: center;
            margin-left: auto;
            font-size: 30px;
            color: $primaryColor;
            padding-left: 15px;
        }
    }
}

.popup{
    display: flex;
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100vh;
    .dim{
        display: block;
        width: 100%;
        height: 100vh;
        background: #000;
        opacity: 0.7;
    }
    .popup_box{
        position: absolute;
        left: 50%;
        top: 50%;
        width: 92%;
        height: auto;
        background: #fff;
        text-align: center;
        margin-left: -46%;
        margin-top: -15%;
        h3{
            color: $primaryColor;
            border-bottom: 1px solid #ccc;
            font-size: 20px;
            padding: 12px 0;
        }
        p{
            padding: 12px;
            font-size: 14px;
            word-break: keep-all;
        }
        .btn_box{
            display: flex;
            justify-content: center;
            border-top: 1px solid #ccc;
            a{
                display: block;
                flex: 1;
                padding: 10px;
            }
            .go{
                background: $primaryColor;
            }
        }
    }
}

@media (max-width: 1200px){
  .container{
     width: 100%;
     padding-right: 0;
     padding-left: 0;
    .inner{
        width: 92%;
    }
    .popup_box{
        left: 50%;
        top: 50%;
        width: 92%;
        margin-left: -46%;
        margin-top: -25%;
    }
  }
}

@media (max-width: 575px){
  .container{
    .popup_box{
        margin-top: -36%;
    }
  }
}
</style>
