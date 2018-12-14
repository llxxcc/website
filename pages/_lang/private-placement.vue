<template>
  <section>
    <Header :url="'/private-placement'"></Header>
    <div class="placement">
      <div class="kv">
        <div class="content">
          <span class="title">{{$t('Placement.Kv.title')}}</span>
          <p>{{$t('Placement.Kv.p1')}}</p>
          <p>{{$t('Placement.Kv.p2')}}</p>
        </div>
        <img v-if="$store.state.locale === 'zh'" width="100%" src="~/assets/landingImgs/kv.jpg" alt="">
        <img v-else width="100%" src="~/assets/landingImgs/kv-en.jpg" alt="">
      </div>
      <div class="use-box">
        <div class="content">
          <span class="title">
            {{$t('Placement.Use.title')}}
          </span>
          <p style="margin-bottom: 20px;">{{$t('Placement.Use.p1')}}</p>
          <p>
            {{$t('Placement.Use.p2')}}
          </p>
          <p>
            {{$t('Placement.Use.p3')}}
          </p>
          <p>
            {{$t('Placement.Use.p4')}}
          </p>
        </div>
      </div>
      <div class="use-box value">
        <div class="content">
          <span class="title">
            {{$t('Placement.Value.title')}}
          </span>
          <p>{{$t('Placement.Value.p1')}}</p>
          <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{$t('Placement.Value.p1-1')}}</p>
          <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{$t('Placement.Value.p1-2')}}</p>
          <p>{{$t('Placement.Value.p2')}}</p>
          <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{$t('Placement.Value.p2-1')}}</p>
          <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{$t('Placement.Value.p2-2')}}</p>
          <p>{{$t('Placement.Value.p3')}}</p>
          <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{$t('Placement.Value.p3-1')}}</p>
          <p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{{$t('Placement.Value.p3-2')}}</p>
          <p>{{$t('Placement.Value.p4')}}</p>
          <p>{{$t('Placement.Value.p5')}}</p>
        </div>
      </div>
      <div class="wallet">
        <div class="content">
          <div class="title">{{$t('Placement.Wallet.title')}}</div>
          <div class="content">
            <p>{{$t('Placement.Wallet.p')}}</p>
            <span class="note">{{$t('Placement.Wallet.tip')}}</span>
            <p>
              {{$t('Placement.Wallet.note')}}
            </p>
          </div>
        </div>
      </div>
      <div class="footer">
        <div class="content">
          <ul>
            <li>
              <a target="_blank" href="https://twitter.com/GOC_Foundation">
                <img src="~/assets/landingImgs/twitter.svg" alt="">
                {{$t('Placement.Footer.twitter')}}
              </a>
            </li>
            <li>
              <a target="_blank" href="https://t.me/GOCfoundationEN">
                <img src="~/assets/landingImgs/telegram.svg" alt="">
                {{$t('Placement.Footer.telegram')}}
              </a>
            </li>
            <li>
              <a target="_blank" href="mailto:support@goc.network">
                <img src="~/assets/landingImgs/mail.svg" alt="">
                {{$t('Placement.Footer.problem')}}
              </a>
            </li>
          </ul>
          <p>Copyright © 2018 goc.network. All rights reserved.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Header from '~/components/landing/Header'

export default {
  components: {
    Header
  },
  data() {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.placement {
  .kv {
    width: 100%;
    position: relative;
    img {
      display: block;
    }
    .content {
      position: absolute;
      width: 29%;
      top: 50%;
      left: 17%;
      transform: translateY(-50%);
      color: #fff;
      .title {
        display: block;
        font-size: 30px;
        color: #FFC100;
        margin-bottom: 40px;
      }
      p {
        color: #C7BFB0;
        line-height: 26px;
      }
      p:nth-child(2) {
        margin-bottom: 18px;
      }
    }
  }
  .use-box {
    background-color: #f2f2f2;
    .content {
      width: 800px;
      margin: 0 auto;
      padding: 60px 0;
      .title {
        display: block;
        width: 100%;
        text-align: center;
        font-size: 30px;
        color: #4E4C46;
        margin-bottom: 50px;
      }
      p {
        line-height: 30px;
      }
    }
  }
  .value {
    background-color: #fff;
    .content {
      p {
        line-height: 30px;
      }
      p:nth-child(2) {
        font-size: 16px;
        font-weight: 400;
        line-height: 30px;
      }
      p:last-child {
        margin-top: 0px;
      }
      .small {
        font-size: 14px;
      }
    }
  }
  .wallet {
    background-color: #f2f2f2;
    .content {
      width: 800px;
      margin: 0 auto;
      padding: 30px 0;
      overflow: hidden;
      .title {
        width: 100%;
        text-align: center;
        font-size: 30px;
        color: #4E4C46;
      }
      > p {
      }
      .note {
        display: block;
        margin-top: 30px;
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
</style>
