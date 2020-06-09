<template>
  <div class="container">
    <div class="top">
      <div class="prev_box">
         <nuxt-link to="/"><img src="../components/arrow-left-solid.svg" alt="이전"></nuxt-link>
      </div>      
      <h2>내 정보</h2>
    </div>

    <section class="info">
      <div class="inner">
        <div class="my">
          <strong>이수민님 <a href=""><img src="../components/fix.png" alt="닉네임수정"></a></strong>
          <div class="btn_wrp">
            <button>카드 설정</button>
            <button>1:1문의</button>
            <button>설정</button>
          </div>
        </div>
        <div class="sns_wrp">
          <p>
            <strong>SNS 연동</strong>
            클릭 한번으로 연락처가 바뀌더라도 혜택을 이어가세요.
          </p>
          <span>
            <a href=""><img src="../components/fb.png" alt="페이스북"></a>
            <a href=""><img src="../components/nv.png" alt="네이버"></a>
            <a href=""><img src="../components/kt.png" alt="카카오톡"></a>
          </span>
        </div>
       </div>   
       <div class="add">
         <a href="">친구 초대하기 &#x003E;</a>        
       </div> 
    </section>
     <div class="tab_box" id="Coupon">
      <div class="inner">
        <h4>히스토리</h4>
        <div class="search_wrp">
          <select name="history" id="">
            <option value="">주문상태(전체)</option>
            <option value="">요청중</option>
            <option value="">주문확인</option>
            <option value="">제조완료</option>
            <option value="">픽업완료</option>
            <option value="">결제취소</option>
          </select>
          <button type="button" onclick="term();" id="modal_term">기간설정</button>
        </div>
        
        <div class="history_box">
          <p class="term">2020.05.08 ~ 2020.06.09</p>
          <nuxt-link to="/">
            <div class="coupon">
              <span class="img_box"><img src="../components/menu_paniniset.png" alt="메뉴히스토리"></span>
              <span>
                <strong>아이스 아메리카노</strong>
                <em>주문  2020.05.27 15:22</em>
                <em>픽업  2020.05.27 15:28</em>
              </span>
              <span class="register">
                <button type="button">간편주문등록</button>
                <em>강남역점</em>
                <em class="primary">1,800원</em>
              </span>
            </div>
          </nuxt-link>
          <nuxt-link to="/">
            <div class="coupon">
              <span class="img_box"><img src="../components/menu_paniniset.png" alt="메뉴히스토리"></span>
              <span>
                <strong>아이스 아메리카노</strong>
                <em>주문  2020.05.20 15:22</em>
                <em>픽업  2020.05.20 15:28</em>
              </span>
              <span class="register">
                <button type="button">간편주문등록</button>
                <em>강남역점</em>
                <em class="primary">1,800원</em>
              </span>
            </div>
          </nuxt-link>
        </div>        
      </div>
    </div>

    <div id="modal" class="modal_term">
      <span class="dim">-</span>
      <div class="modal_content">
        <h2 class="primary">기간설정</h2>
        <p class="start">시작일 <button type="button">2020.05.09</button></p>
        <p class="fin">종료일 <button type="button">2020.06.09</button></p>
        <div class="set_term">
          <input type="radio">1년
          <input type="radio">1개월
          <input type="radio">기간설정
        </div>
        <span class="search_info">최근 1년까지의 이력만 조회가능합니다.</span>
        <div class="btn_box">
          <nuxt-link to="/mypage">취소</nuxt-link>
          <nuxt-link to="/mypage">확인</nuxt-link>
        </div>
      </div>
    </div>
  </div>
  
</template>

<script>
export default {
    head: {
      title: '마이페이지 바나프레소',
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
function term(){
  document.getElementById("modal_term").style.display = "block";
}
</script>

<style lang="scss" scoped>
$primaryColor: #f66b91;
ul{margin: 0;padding: 0;}
li{list-style: none;}
a{color: #1a1a1a;text-decoration: none;}
p{margin: 0;}
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR&display=swap');
.primary{color: $primaryColor;}

.container {
    width: 575px;
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
    .inner{
        display: flex;
        flex-direction: column;
        width: 96%;
        margin: 0 auto;
        padding: 20px 0 0;
    }
    .info{
      background: #f7f7f7;
      .my{
        display: flex;
        .btn_wrp{
          margin-left: auto;
          button{
            border: 1px solid #ccc;
            background: #fff;
            color: #ccc;
            font-size: 12px;
          }
        }
      }
    }
    .sns_wrp{
      display: flex;
      margin: 8px 0;
      p{
        font-size: 12px;
        word-break: keep-all;
        strong{
          display: block;
          color: $primaryColor;
          font-size: 14px;
        }
      }
      span{
        display: flex;
        margin-left: auto;
        a{
          display: flex;
          width: 36px;
          height: 36px;
          margin: 0 4px;
          border-radius: 50%;
          align-items: center;
          justify-content: center;
          &:nth-child(1){background: #4276b2;}
          &:nth-child(2){background: #48ab10;}
          &:nth-child(3){background: #ffee01;}
        }
      }      
    }
    .add{
      border-top: 1px solid #ccc;
      text-align: center;
      a{
        display: block;
        padding: 8px 0;
      }
    }
    .search_wrp{
      display: flex;
      font-size: 14px;
      select{
        flex: 2;
        border: 1px solid $primaryColor;
        padding: 8px;
      }
      button{
        flex: 1;
        color: #fff;
        border: 1px solid $primaryColor;
        margin-left: 8px;
        padding: 8px;
        background: $primaryColor;
      }
    }
    .history_box{
      .term{
        margin: 12px 0 0 0;
        font-size: 14px;
        color: #333;
      }
      .register{
        margin-left: auto;
        text-align: right;
        button{
          background: $primaryColor;
          color: #fff;
          border: 1px solid $primaryColor;
          font-size: 12px;
        }
      }
    }
    .coupon_list{
        display: flex;
        .btn_wrp{
          margin-left: auto;
          button{
            border: 1px solid #ccc;
            background: #fff;
            color: #ccc;
            font-size: 12px;
          }
        }        
      }
      .coupon{
        display: flex;
        border: 1px solid #ccc;
        font-size: 14px;
        color: #333;
        background: #fff;
        padding: 12px;
        margin-bottom: 12px;
        .img_box{
          display: flex;
          align-items: center;
          margin-right: 12px;
          width: 20%;
          img{
            width: 100%;
          }
        }
        strong{
          display: block;
        }
        em{
          display: block;
          font-style: inherit;
          font-size: 12px;
        }
      }       
}
#modal{
  &.modal_term{
    .dim{
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100vh;
      background: #000;
      opacity: 0.5;
    }
    .modal_content{
      position: absolute;
      left: 50%;
      top: 50%;
      margin-left: -35%;
      margin-top: -35%;
      z-index: 20;
      width: 70%;
      background: #fff;
      border-radius: 4px;
      box-shadow: 1px 2px 3px #ccc;
      padding: 12px 0;
      h2{font-weight: bold;text-align: center;font-size: 16px;padding-bottom: 12px;margin: 0;border-bottom: 1px solid #ccc;}
      .start,.fin{
        display: flex;
        padding: 6px 12px;
        font-size: 14px;
        border-bottom: 1px solid #eee;
        button{
          background: transparent;
          border: none;
          margin-left: auto;
        }
      }
      .set_term{
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 12px 0;
        font-size: 14px;
        input{
          margin: 0 8px;
        }
      }
      .search_info{
        display: block;
        font-size: 12px;
        text-align: center;
        color: #ccc;
      }
      .btn_box{
        display: flex;
        padding: 16px 12px 0 12px;
        a{
          flex: 1;
          background: #333;
          color: #fff;
          text-align: center;
          padding: 6px 0;
          &:last-child{
            background: $primaryColor;
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
    .inner{
      width: 96%;
      margin: auto;
    }
    .coupon{
      .img_box{
        width: 20%;
        img{
          width: 100%;
        }
      }
    }
  }
}
</style>
