<template>
<div class="index">
  <Header :page.sync="page"/>
  <div class="fullpage-wp" ref="fullpage">
    <div id="page1" name="page1" class="page-1 page">
      <div class="content">
        <div class="text1">{{$t('Index.page1.t1')}}</div>
        <div class="text2">{{$t('Index.page1.t2')}}</div>
        <div class="text3">
          <p>{{$t('Index.page1.p1')}}</p>
          <p>{{$t('Index.page1.p2')}}</p>
          <p>{{$t('Index.page1.p3')}}</p>
        </div>
        <a href="https://market.goc.network" target="_blank">{{$t('Index.page1.btn1')}}</a>
        <nuxt-link :to="'/' + $store.state.locale + '/use-goc'" target="_blank">{{$t('Index.page1.btn2')}}</nuxt-link>
      </div>
      <img
          class="orn"
          src="~/assets/imgs/orn1.png"
          width="186">
    </div>
    <div id="page2" name="page2" class="page-2 page">
      <div class="content">
        <div
          class="line">
        </div>
        <div
          class="text">
          {{$t('Index.page2.t')}}
        </div>
        <div class="text1">
          <p>
            {{$t('Index.page2.p1')}}
          </p>
          <p>
            {{$t('Index.page2.p2')}}
          </p>
          <p>
            {{$t('Index.page2.p3')}}
          </p>
          <p>
            {{$t('Index.page2.p4')}}
          </p>
        </div>
        <div class="btn">
          <a href="https://market.goc.network" target="_blank">{{$t('Index.page2.btn')}}</a>
        </div>
      </div>
      <img
        class="orn"
        src="~/assets/imgs/orn1.png"
        width="186">
      <!-- <img
        class="orn1"
        src="~/assets/imgs/orn2.png"> -->
    </div>
    <div id="page3" name="page3" class="page-3 page">
      <div class="content">
        <div class="line">
        </div>
        <div class="text">
          {{$t('Index.page3.t')}}
        </div>
        <ul>
          <li>
            <span class="title">{{$t('Index.page3.item1-t')}}</span>
            <span class="description">
              <i class="circle"></i>
              <span>{{$t('Index.page3.item1-p1')}}</span>
            </span>
            <span class="description">
              <i class="circle"></i>
              <span>{{$t('Index.page3.item1-p2')}}</span>
            </span>
            <img src="../../assets/imgs/icon-1.png" alt="">
          </li>
          <li>
            <span class="title">{{$t('Index.page3.item2-t')}}</span>
            <span class="description">
              <i class="circle"></i>
              <span>{{$t('Index.page3.item2-p1')}}</span>
            </span>
            <span class="description">
              <i class="circle"></i>
              <span>{{$t('Index.page3.item2-p2')}}</span>
            </span>
            <img src="../../assets/imgs/icon-2.png" alt="">
          </li>
          <li>
            <span class="title">{{$t('Index.page3.item3-t')}}</span>
            <span class="description">
              <i class="circle"></i>
              <span>
                {{$t('Index.page3.item3-p1')}}
              </span>
            </span>
            <span class="description">
              <i class="circle"></i>
              <span>{{$t('Index.page3.item3-p2')}}</span>
            </span>
            <img src="../../assets/imgs/icon-3.png" alt="">
          </li>
        </ul>
      </div>
      <img src="../../assets/imgs/orn3.png" alt="" class="orn1">
    </div>
    <div id="page4" name="page4" class="page-4 page">
      <div class="content">
        <div class="line"> 
        </div>
        <div class="text">
          {{$t('Index.page4.t')}}
        </div>
        <div class="text1">
          <p>
            {{$t('Index.page4.p1')}}
          </p>
          <p>
            {{$t('Index.page4.p2')}}
          </p>
          <p>
            {{$t('Index.page4.p3')}}
          </p>
        </div>
      </div>
      <img src="../../assets/imgs/orn3.png" alt="" class="orn">
    </div>
    <div id="page5" name="page5" class="page-5 page">
      <ul>
        <li class="time">
          <span class="line"></span>
          <span>2018.12.03</span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item1-p1')}}
          </span>
        </li>
      </ul>
      <ul>
        <li class="time">
          <span class="line"></span>
          <span>2018.12.30</span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item2-p1')}}
          </span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item2-p2')}}
          </span>
        </li>
      </ul>
      <ul>
        <li class="time">
          <span class="line"></span>
          <span>2019 Q1</span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item3-p1')}}
          </span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item3-p2')}}
          </span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item3-p3')}}
          </span>
        </li>
        <li class="project">
          <span>{{$t('Index.page5.item3-project1')}}</span>
          <span>{{$t('Index.page5.item3-project2')}}</span>
        </li>
        <li class="project">
          <span>{{$t('Index.page5.item3-project3')}}</span>
          <span>{{$t('Index.page5.item3-project4')}}</span>
        </li>
        <li class="project">
          <span>{{$t('Index.page5.item3-project5')}}</span>
          <span>{{$t('Index.page5.item3-project6')}}</span>
        </li>
      </ul>
      <ul>
        <li class="time">
          <span class="line"></span>
          <span>2019 Q2</span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item4-p1')}}
          </span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
            {{$t('Index.page5.item4-p2')}}
          </span>
        </li>
      </ul>
      <ul>
        <li class="time">
          <span class="line"></span>
          <span>2019 Q3</span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
             {{$t('Index.page5.item5-p1')}}
          </span>
        </li>
        <li class="item">
          <span class="circle"></span>
          <span class="text">
             {{$t('Index.page5.item5-p2')}}
          </span>
        </li>
      </ul>
    </div>
    <div class="footer">
      <div class="content">
        <ul>
          <li>
            <a target="_blank" href="https://twitter.com/GOC_Foundation">
              <img src="~/assets/imgs/twitter.svg" alt="">
              {{$t('Index.Footer.twitter')}}
            </a>
          </li>
          <li>
            <a target="_blank" href="https://t.me/GOCfoundationEN">
              <img src="~/assets/imgs/telegram.svg" alt="">
              {{$t('Index.Footer.telegram')}}
            </a>
          </li>
          <li>
            <a target="_blank" href="mailto:support@goc.network">
              <img src="~/assets/imgs/mail.svg" alt="">
              {{$t('Index.Footer.problem')}}
            </a>
          </li>
        </ul>
        <p>Copyright © 2018 goc.network. All rights reserved.</p>
      </div>
    </div>
  </div>
  
  <!-- <a target="_blank" href="https://twitter.com/GOC_Foundation" class="twitter">
    <img src="~/assets/imgs/twitter.svg" alt="">
  </a>
  <a target="_blank" href="https://t.me/GOCfoundationEN" class="tele">
    <img src="~/assets/imgs/tele.svg" alt="">
  </a> -->
</div>
</template>

<script>
import Header from '~/components/Header'

export default {
  components: {
    Header
  },
  created() {
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  data() {
    return {
      opts: {
        start: 0,
        dir: 'v',
        loop: false,
        duration: 0,
        beforeChange: (dom, next, curr) => {
          this.page = curr
        },
      },
      page: 0
    }
  },
  methods: {
    moveTo(page){
      this.$refs.fullpage.$fullpage.moveTo(page); //Move to the next page
    },
    handleScroll() {
      let scrollTop = document.body.scrollTop + document.documentElement.scrollTop
      let windowH = window.innerHeight
      this.page = Math.round(scrollTop / windowH)
    }
  },
  watch: {
    page: function (n, o) {
      console.log(n, o)
    }
  }
}
</script>

<style lang="scss" scope>
.index {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  min-width: 1200px;
  height: 100vh;
  color: #FFFFFF;
  .fullpage-wp {
     height: 100%;
    .page {
      position: relative;
      overflow: hidden;
      height: 100%;
      min-height: 650px;
      .content {
        .line {
          width: 50px;
          height: 3px;
          border-radius: 8px;
          background-color: #ffc100;
          margin-bottom: 40px;
        }
        .text {
          font-size: 30px;
          color: #FFC100;
          letter-spacing: 2.67px;
          line-height: 33px;
          margin-bottom: 30px;
        }
      }
    }
    .page-1 {
      background: url('../../assets/imgs/kv.png') no-repeat center;
      background-size: cover;
      .content {
        position: absolute;
        top: 30.5%;
        left: 50%;
        transform: translateX(-50%);
        text-align: center;
        .text1 {
          font-size: 84px;
          letter-spacing: 10.04px;
          font-weight: 600;
        }
        .text2 {
          font-size: 64px;
          letter-spacing: 10px;
          margin-bottom: 40px;
          font-weight: 200;
        }
        .text3 {
          font-size: 16px;
          line-height: 30px;
          color: #FFF6E7;
          letter-spacing: 0.24px;
          font-weight: 350;
          p {
            white-space: nowrap;
          }
          p:nth-child(3) {
            width: 96%;
            white-space: inherit;
            word-break: break-all;
          }
        }
        a {
          display: inline-block;
          width: 130px;
          height: 43px;
          line-height: 42px;
          border: 1px solid #FFC100;
          border-radius: 4px;
          background: transparent;
          color: #FFC100;
          font-size: 14px;
          outline-style: none;
          text-decoration: none;
          cursor: pointer;
          margin: 65px 50px 0 0;
        }
        a:last-child {
          margin-right: 0px;
        }
        a:hover {
          background-color: #FFC100;
          color: #fff;
        }
      }
      .orn {
        position: absolute;
        bottom: -234px;
        right: 0px;
      }
    }
    .page-2 {
      background: url('../../assets/imgs/Market.png') no-repeat center;
      background-size: cover;
      .content {
        width: 28%;
        position: absolute;
        top: 50%;
        left: 14.3%;
        transform: translateY(-50%);
        .text1 {
          p {
            font-size: 14px;
            color: #FFF6E7;
            letter-spacing: 0.03px;
            line-height: 24px;
            margin-bottom: 18px;
          }
          p:last-child {
            margin: 0;
          }
        }
        .btn {
          width: 100%;
          a {
            display: inline-block;
            width: 130px;
            height: 43px;
            line-height: 42px;
            border: 1px solid #FFC100;
            text-align: center;
            border-radius: 4px;
            background: transparent;
            color: #FFC100;
            font-size: 14px;
            text-decoration: none;
            outline-style: none;
            cursor: pointer;
            margin-top: 30px;
          }
          a:hover {
            background-color: #FFC100;
            color: #fff;
          }
        }
      }
      .orn {
        position: absolute;
        top: -234px;
        right: 0px;
      }
      .orn1 {
        width: 1200px;
        position: absolute;
        right: 0px;
        bottom: -11%;
      }
    }
    .page-3 {
      background: url('../../assets/imgs/token.png') no-repeat center;
      background-size: cover;
      .content {
        position: absolute;
        top: 15%;
        left: 50%;
        transform: translateX(-50%);
        overflow: hidden;
        .text {
          margin-bottom: 135px;
        }
        ul {
          width: 1020px;
          list-style: none;
          margin: 0px;
          padding: 0px;
          li {
            position: relative;
            float: left;
            width: 320px;
            height: 240px;
            padding-top: 75px;
            background: rgba(226, 191, 129, .1);
            margin-right: 30px;
            border-radius: 4px;
            border: 3px solid #A0917A;
            color: #FFF6E7;
            .title {
              display: block;
              text-align: center;
              font-size: 18px;
              letter-spacing: 0.04px;
              line-height: 24px;
              margin-bottom: 20px;
            }
            .description {
              display: block;
              padding: 0 20px 0 26px;
              margin-bottom: 10px;
              font-size: 14px;
              .circle {
                display: inline-block;
                width: 6px;
                height: 6px;
                border-radius: 100%;
                background-color: #fff6e7;
              }
            }
            img {
              width: 130px;
              position: absolute;
              top: -75px;
              left: 50%;
              transform: translateX(-50%);
            }
          }
          li:last-child {
            margin: 0px;
          }
        }
      }
      .orn {
        position: absolute;
        width: 1000px;
        left: 0;
        top: -17%;
      }
      .orn1 {
        position: absolute;
        right: -100px;
        bottom: -170px;
      }
    }
    .page-4 {
      background: url('../../assets/imgs/DApp.png') no-repeat center;
      background-size: cover;
      .content {
        width: 28%;
        position: absolute;
        top: 48%;
        right: 12.3%;
        transform: translateY(-50%);
        .text1 {
          p {
            font-size: 14px;
            color: #FFF6E7;
            letter-spacing: 0.03px;
            line-height: 24px;
            margin-bottom: 18px;
          }
          p:last-child {
            margin: 0;
          }
        }
      }
      .orn {
        position: absolute;
        right: -100px;
        top: -174px;
      }
    }
    .page-5 {
      background: url('../../assets/imgs/time.png') no-repeat center;
      background-size: cover;
      ul {
        font-size: 12px;
        list-style: none;
        position: absolute;
        color: #FFF6E7;
        li {
          overflow: hidden;
          display: block;
          margin-bottom: 8px;
          span {
            float: left;
          }
          span:first-child {
            margin-right: 15px;
          }
        }
        .time {
          color: #FFC100;
          letter-spacing: 0.03px;
          font-weight: 600;
          .line {
            display: block;
            width: 2px;
            height: 14px;
            background-color: #ffc100;
            margin-top: 2px;
            margin-right: 17px;
          }
        }
        .item {
          .circle {
            width: 6px;
            height: 6px;
            background-color: rgba(255,255,255,0.40);
            border-radius: 100%;
            margin-top: 7px;
          }
          .text {
            width: 200px;
          }
        }
      }
      ul:first-child {
        top: 29%;
        left: 5%;
      }
      ul:nth-child(2) {
        top: 31%;
        left: 22%;
        .item {
          .text {
            width: 260px;
          }
        }
      }
      ul:nth-child(3) {
        top: 19%;
        left: 43%;
        .project {
          span:first-child {
            display: inline-block;
            margin: 0 20px;
          }
        }
      }
      ul:nth-child(4) {
        top: 38%;
        right: 18%;
        .item {
          .text {
            width: 255px;
          }
        }
      }
      ul:nth-child(5) {
        top: 28%;
        right: 4%;
        .item {
          .text {
            width: 210px;
          }
        }
      }
    }
    .footer {
      width: 100%;
      height: 120px;
      background-color: #272622;
      position: relative;
      .content {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        font-size: 14px;
        color: #C7BFB0;
        text-align: center;
        ul {
          display: block;
          overflow: hidden;
          list-style: none;
          margin-bottom: 20px;
          padding-left: 0px;
          li {
            float: left;
            padding: 0 20px;
            a {
              color: #C7BFB0;
              text-decoration: none;
            }
          }
          li:nth-child(2) {
            border-left: 1px solid #93948f;
            border-right: 1px solid #93948f;
          }
          li:first-child {
            padding-left: 0px;
          }
          li:last-child {
            padding-right: 0px;
          }
        }
        p {
          font-size: 12px;
        }
      }
    }
  }
  
  .tele {
    position: fixed;
    right: 20px;
    bottom: 90px;
  }
  .twitter {
    position: fixed;
    right: 20px;
    bottom: 40px;
  }
}
@media (min-width: 1950px) {
.index {
  .fullpage-wp {
    .page-1 {
      .content {
        .text1 {
          font-size: 135px;
          letter-spacing: 20px;
        }
        .text2 {
          font-size: 100px;
          letter-spacing: 46px;
          margin-bottom: 60px;
        }
        .text3 {
          font-size: 26px;
          line-height: 40px;
        }
        a {
          width: 170px;
          height: 63px;
          font-size: 20px;
          line-height: 62px;
          margin-top: 90px;
        }
      }
    }
    .page-2 {
      .content {
        width: 22%;
        left: 22.3%;
        .line {
          margin-bottom: 60px;
        }
        .text {
          font-size: 60px;
          margin-bottom: 60px;
        }
        .text1 {
          p {
            font-size: 20px;
            line-height: 34px;
            margin-bottom: 60px;
          }
        }
      }
      .orn1 {
        width: 1920px;
        bottom: -18%;
      }
    }
    .page-3 {
      .content {
        .line {
          margin-bottom: 60px;
        }
        .text {
          font-size: 60px;
          margin-bottom: 225px;
        }
        ul {
          width: 1500px;
          li {
            width: 480px;
            height: 350px;
            padding-top: 130px;
            .title {
              font-size: 28px;
              margin-bottom: 48px;
            }
            .description {
              padding: 0 80px 0 100px;
              font-size: 18px;
            }
            img {
              width: 160px;
            }
          }
        }
      }
      .orn {
        position: absolute;
        width: 1720px;
        left: 0;
        top: -16%;
      }
      .orn1 {
        position: absolute;
        right: -80px;
        bottom: -130px;
      }
    }
    .page-4 {
      .content {
        width: 22%;
        right: 18.3%;
        .line {
          margin-bottom: 60px;
        }
        .text {
          font-size: 60px;
          margin-bottom: 60px;
        }
        .text1 {
          p {
            font-size: 20px;
            line-height: 34px;
            margin-bottom: 60px;
          }
        }
      }
      .orn {
        right: -80px;
        top: -185px;
      }
    }
    .page-5 {
      ul {
        font-size: 14px;
        .item {
          .text {
            width: 230px;
          }
        }
      }
      ul:first-child {
        top: 33%;
        left: 6%;
      }
      ul:nth-child(2) {
        top: 37%;
        left: 20%;
        .item {
          .text {
            width: 300px;
          }
        }
      }
      ul:nth-child(3) {
        top: 32%;
      }
      ul:nth-child(4) {
        top: 44%;
        right: 20%;
        .item {
          .text {
            width: 295px;
          }
        }
      }
      ul:nth-child(5) {
        top: 33%;
        right: 5%;
        .item {
          .text {
            width: 250px;
          }
        }
      }
    }
  }
}
}
@media (max-width: 1370px) {
  .index {
    .fullpage-wp {
      .page-5 {
        ul:nth-child(2) {
          top: 25%;
          .item {
            .text {
              width: 200px;
            }
          }
        }
        ul:nth-child(3) {
          left: 41%;
        }
        ul:nth-child(4) {
          top: 33%;
          right: 22%;
          .item {
            .text {
              width: 180px;
            }
          }
        }
        ul:nth-child(5) {
          top: 27%;
          right: 4%;
          .item {
            .text {
              width: 210px;
            }
          }
        }
      }
    }
  }
}
</style>
