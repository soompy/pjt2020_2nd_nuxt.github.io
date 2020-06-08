<template>
  <div class="container">
    <div class="top">
      <div class="prev_box">
         <nuxt-link to="/"><img src="../components/arrow-left-solid.svg" alt="이전"></nuxt-link>
      </div>      
      <h2>멤버십</h2>
    </div>
    <ul class="membership">
      <li>스탬프 <span>/12</span></li>
      <li>쿠폰 <span>1</span></li>
      <li>바나포인트 <span>P</span></li>
    </ul> 
    <div class="tab_box">
      <div class="couponWrp">
        <h3>바나프레소</h3>
        <ul class="coupon">
          <li class="on"></li>
          <li class="on"></li>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
          <li class="finish"></li>
        </ul>
      </div>
      <dl class="rule">
        <dt><p>스탬프 적립카드 <strong class="primary">유의사항</strong> 안내</p> <a href="#" class="toggle_slide"><img src="../components/sort-down-solid.svg" alt="&#812;"></a></dt>
        <dd>제조 음료 1잔당 1개의 스탬프가 픽업 시 적립 완료됩니다.</dd>
        <dd>스탬프 적립 제외: 병음료, 베이커리, 할인메뉴, 무료쿠폰 사용 음료</dd>
        <dd><strong>스탬프 1개 적립 시 무료 쿠폰이 다음날 발급되며, 구매했던 12잔 음료 내에서 사용 가능합니다.</strong></dd>
        <dd>스탬프 유효기간은 적립일로부터 1년입니다.</dd>
        <dd>스탬프 및 쿠폰은 바나프레소 전 지점에서 적립 및 사용 가능합니다.</dd>
      </dl>
      <section class="history">
        <div class="inner">
          <p class="tit"><strong>적립 및 사용 내역</strong><em>최근 6개월간 내역입니다.</em></p>
          <ul class="used">
            <li>
              <p><strong>APP 주문</strong><em class="date">2020.05.27</em></p>
              <span>적립<em>1</em></span>
            </li>
            <li>
              <p><strong>APP 주문</strong><em class="date">2020.05.20</em></p>
              <span>적립<em>2</em></span>
            </li>
            <li>
              <p><strong>APP 주문</strong><em class="date">2020.05.17</em></p>
              <span>적립<em>5</em></span>
            </li>
            <li>
              <p><strong>APP 주문</strong><em class="date">2020.05.14</em></p>
              <span>적립<em>1</em></span>
            </li>
            <li>
              <p><strong>APP 주문</strong><em class="date">2020.05.12</em></p>
              <span>적립<em>3</em></span>
            </li>
            <li>
              <p><strong>APP 주문</strong><em class="date">2020.05.07</em></p>
              <span>적립<em>1</em></span>
            </li>
          </ul>
        </div>
      </section>
    </div>
    <div class="tab_box">
      
    </div>
    <div class="tab_box">
      
    </div>

  </div>
</template>

<script>
export default {
    head: {
      title: '선택화면 바나프레소',
      meta: [
        { hid: 'description', name: 'description', content: '바나프레소 모바일 결제' }
      ],
      noscript: [
        { innerHTML: 'Body No Scripts', body: true }
      ]
    }
  }  
</script>
<script>
export default{
  asyncData(){
    return new Promise((resolve) => {
      setTimeout(function(){
        resolve({ set: '베이컨파니니세트' })
      },1000);
    })
  }
}
</script>

<style lang="scss" scoped>
$primaryColor: #f66b91;
ul{margin: 0;padding: 0;}
li{list-style: none;}
a{color: #1a1a1a;}
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap');
.primary{color: $primaryColor;}

.container {
    width: 575px;
    height: 100vh;
    font-family: 'Noto Sans KR', sans-serif;
    box-shadow: 1px 1px 5px 3px #ccc;
    border-radius: 6px;
    padding: 0;
    .prev_box{
      margin-right: auto;
      a{
          display: block;
          width: 16px;
          height: 16px;
      }
    }
    .top{
      display: flex;
      padding: 16px;
      h2{
        font-size: 20px;
        margin-bottom: 0;
        margin-right: auto;
      }
    }
    .membership{
      display: flex;
      background: #1a1a1a;
      padding: 10px 0;
      color: #fff;
      font-size: 14px;
      li{
        flex: 1;
        text-align: center;
        span{
          display: block;
        }
        &:nth-child(even){
          border-left: 1px solid #ccc;
          border-right: 1px solid #ccc;
        }
      }    
    }
    .couponWrp{
      background: #edc8ae;
      h3{
        background: #ddb89d;
        padding: 8px 16px;
        font-size: 16px;
        margin: 0;
      }
      .coupon{
        padding: 10px 16px;
        height: 142px;
        li{
          float: left;
          width: 20%;
          height: 62px;
          background: url("../components/coupon_off.png") center 0 no-repeat;
          &.on{
            background: url("../components/coupon_on.png") center 0 no-repeat;
          }
          &.finish{
            background: url("../components/coupon_fin.png") center 0 no-repeat;
          }
        }
      }
    }
    .inner{
        display: flex;
        flex-direction: column;
        width: 96%;
        margin: 0 auto;
        padding: 20px 0;
    }
    .rule{
      margin-bottom: 0;
        dt{
          display: flex;
          width: 96%;
          margin: auto;
          padding: 8px 0;
          border-bottom: 1px solid #eee;
          p{margin: auto 0;}
          strong{
            display: contents;
          }
          .toggle_slide{
            width: 12px;
            margin-left: auto;
            img{
              display: flex;
              align-items: center;
            }
          }
        }
        dd{
          position: relative;
          font-size: 14px;
          padding: 6px 16px 6px 26px;
          margin: 0;
          word-break: keep-all;
          background: #eee;
          &:before{
            display: block;
            clear: both;
            content: '*';
            position: absolute;
            left: 14px;
            top: 10px;
            width: 4px;
            height: 4px;
            margin-top: -2px;
            padding-right: 10px;
            font-size: 12px;
          }
        }
      }
      .history{
        .tit{
          font-size: 14px;
          em{
            display: block;
            font-style: inherit;
            font-size: 12px;
            color: #999;
          }
        }
        .used{
          height: 20vh;
          overflow: scroll;
          border-top: 2px solid #ccc;
          li{
            display: flex;
            border-bottom: 1px solid #ccc;
            padding: 8px 0;
            p{
              font-size: 14px;
              margin: 0;
            }
            .date{
              display: block;
              font-style: inherit;
              font-size: 12px;
              color: #ccc;
            }
            span{
              font-size: 14px;
              margin-left: auto;
              text-align: center;
              color: #226cb4;
              em{
                display: block;
                font-style: inherit;
                font-size: 12px;
                font-weight: bold;
              }
            }
          }
        }
      }
}

@media (max-width: 575px){
  .container{
    width: 100%;
    height: auto;
    padding: 0 2%;
    .inner{
      width: 100%;
    }
  }
}
</style>
