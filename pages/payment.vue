<template>
  <div class="container">
    <div class="inner">
      <div class="close_box">
        <nuxt-link to="/best"><img src="../components/times-solid.svg" alt="닫기"></nuxt-link>
      </div>
      <div class="top">
        <h2>{{ set }} <span>4,500원</span></h2>
        <p>고소한 아메리카노와 수제 베이컨 파니니로 활기찬 하루를 시작하세요.</p>
      </div>
      <section class="choice_box">
        <div class="product">
          <span><img src="../components/menu_paniniset.png" alt="베이컨파니니세트"></span>
        </div>
        <div class="choice">
          <div class="number">
            <p class="hot">HOT <span class="kor">따뜻한 음료</span></p>
            <p class="counter_box">
              <button class="subtraction">&#x002D;</button>
              <span class="count">0</span>
              <button class="add">&#x002B;</button>
            </p>
          </div>
          <div class="number">
            <p class="ice">ICE <span class="kor">차가운 음료</span></p>
            <p class="counter_box">
              <button class="subtraction">&#x002D;</button>
              <span class="count">0</span>
              <button class="add">&#x002B;</button>
            </p>
          </div>
        </div>
      </section>
      <a href="" class="order">확인</a>
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
<script>
  
</script>

<style lang="scss" scoped>
$primaryColor: #f66b91;
// .container{min-height: auto !important;}
ul{margin: 0;padding: 0;}
li{list-style: none;}
a{color: #1a1a1a;}
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap');

.container {
    display: flex;
    width: 575px;
    height: 100vh;
    font-family: 'Noto Sans KR', sans-serif;
    box-shadow: 1px 1px 5px 3px #ccc;
    border-radius: 6px;
    .inner{
        display: flex;
        flex-direction: column;
        width: 96%;
        height: 100vh;  
        margin: 0 auto;
        padding: 40px 0;
        .close_box{
          margin-left: auto;
          a{
            display: block;
            width: 16px;
            height: 16px;
          }
        }
        .top{
          h2{
            text-align: center;
            font-size: 20px;
            span{font-size: 16px;color: $primaryColor;}
          }
          p{color: #333;text-align: center;font-size: 14px;word-break: keep-all;}
        }
        .choice_box{
          display: flex;
          align-items: center;
          .product{
            flex: 1;
          }
          .choice{
            flex: 2;
            .number{
              display: flex;
              p{
                font-size: 18px;
                text-align: center;
                flex: 1;
                font-weight: bold;
                .kor{display: block;font-size: 14px;}
                &.hot{color: #c50707;}
                &.ice{color: #226cb4;}
              }
              .counter_box{
                display: flex;
                flex: 2;
                margin-left: auto;
                button{
                  width: 50px;
                  height: 50px;
                  background: #fff;
                  border: 1px solid #ccc;                  
                }
                .subtraction{margin-right: auto;}
                .count{margin: auto;}
                .add{
                  margin-left: auto;
                }
              }
            }
          }
        }
    }
    .order{
      display: block;
      width: 100%;
      color: #fff;
      background: $primaryColor;
      padding: 10px 0;
      text-align: center;
      margin-top: auto;
    }
}

@media (max-width: 575px){
  .container{
    width: 100%;
    .inner{
      width: 100%;
      .choice_box{
        .product{
          display: flex;
          width: 20%;
          justify-content: center;
          img{width: 100%;}
        }
        .choice{
          .number{
            p{
              font-size: 14px;
              margin-right: 4px;
              .kor{font-size: 12px;}
            }
            .counter_box{
              button{
                width: 40px;
                height: 40px;
              }
            }
          }
        }
      }
    }
  }
}
</style>
