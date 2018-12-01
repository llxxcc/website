<template>
  <section>
    <Header></Header>
    <div class="index">
      <div class="kv">
        <div class="content">
          <span class="title">{{$t('GocToken.Kv.title')}}</span>
          <p>{{$t('GocToken.Kv.p1')}}</p>
          <p>{{$t('GocToken.Kv.p2')}}</p>
        </div>
        <img v-if="$store.state.locale === 'zh'" width="100%" src="~/assets/landingImgs/kv.jpg" alt="">
        <img v-else width="100%" src="~/assets/landingImgs/kv-en.jpg" alt="">
      </div>
      <div class="value">
        <div class="content">
          <div class="title">{{$t('GocToken.Value.title')}}</div>
          <ul>
            <li :class="$store.state.locale === 'en' ? 'lengthen' : ''" v-for="(v, i) in vals" :key="i">
              <img :src="v.img" alt="">
              <p class="item-title">
                {{v.title}}
              </p>
              <p class="item-text" v-for="(p, n) in v.text" :key="n">
                {{p}}
              </p>
            </li>
          </ul>
        </div>
      </div>
      <div class="wallet">
        <div class="content">
          <div class="title">{{$t('GocToken.Wallet.title')}}</div>
          <ul>
            <li v-for="(w, i) in wallets" :key="i">
              <img 
                :src="$store.state.locale === 'en' ? w.en : w.zh"
                alt="">
              <span class="name">{{w.name}}</span>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer">
        <div class="content">
          <ul>
            <li>
              <a target="_blank" href="https://twitter.com/GOC_Foundation">
                <img src="~/assets/landingImgs/twitter.svg" alt="">
                {{$t('GocToken.Footer.twitter')}}
              </a>
            </li>
            <li>
              <a target="_blank" href="https://t.me/GOCfoundationEN">
                <img src="~/assets/landingImgs/telegram.svg" alt="">
                {{$t('GocToken.Footer.telegram')}}
              </a>
            </li>
            <li>
              <a target="_blank" href="mailto:support@goc.network">
                <img src="~/assets/landingImgs/mail.svg" alt="">
                {{$t('GocToken.Footer.problem')}}
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
      vals: [
        {img: require('~/assets/landingImgs/icon1.png'), title: this.$t('GocToken.Value.item1-title'), text: this.$t('GocToken.Value.item1-text')},
        // {img: require('~/assets/landingImgs/icon2.png'), title: this.$t('GocToken.Value.item2-title'), text: this.$t('GocToken.Value.item2-text')},
        {img: require('~/assets/landingImgs/icon3.png'), title: this.$t('GocToken.Value.item3-title'), text: this.$t('GocToken.Value.item3-text')},
        {img: require('~/assets/landingImgs/icon4.png'), title: this.$t('GocToken.Value.item4-title'), text: this.$t('GocToken.Value.item4-text')},
        {img: require('~/assets/landingImgs/icon5.png'), title: this.$t('GocToken.Value.item5-title'), text: this.$t('GocToken.Value.item5-text')}
      ],
      wallets: [
        {zh: require('~/assets/landingImgs/itron.png'), en: require('~/assets/landingImgs/itron.png'), name: this.$t('GocToken.Wallet.item1-name')},
        {zh: require('~/assets/landingImgs/cobo.png'), en: require('~/assets/landingImgs/cobo.png'), name: this.$t('GocToken.Wallet.item2-name')},
        {zh: require('~/assets/landingImgs/math.png'), en: require('~/assets/landingImgs/math-en.png'), name: this.$t('GocToken.Wallet.item3-name')}
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.index {
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
  .value {
    background-color: #fff;
    .content {
      overflow: hidden;
      width: 1100px;
      margin: 0 auto;
      padding: 60px 0;
      .title {
        width: 100%;
        text-align: center;
        font-size: 30px;
        color: #4E4C46;
        margin-bottom: 50px;
      }
      > ul {
        list-style: none;
        width: 100%;
        li {
          float: left;
          width: 32%;
          height: 370px;
          text-align: center;
          margin-right: 1.5%;
          padding: 20px 32px 0 32px;          
          background-color: #f3f3f3;
          border-radius: 1px;
          margin-bottom: 28px;
          img {
            width: 160px;
          }
          .item-title {
            font-size: 18px;
            color: #4E4C46;
            margin-bottom: 17px;
          }
          .item-text {
            text-align: left;
            width: 100%;
            font-size: 15px;
            line-height: 21px;
            color: #97948F;
          }
        }
        li:nth-child(3n + 3) {
          margin-right: 0;
        }
        .lengthen {
          height: 420px;
        }
      }
    }
  }
  .wallet {
    background-color: #f2f2f2;
    .content {
      width: 1100px;
      margin: 0 auto;
      padding: 60px 0;
      overflow: hidden;
      .title {
        width: 100%;
        text-align: center;
        font-size: 30px;
        color: #4E4C46;
        margin-bottom: 50px;
      }
       > ul {
        list-style: none;
        width: 100%;
        li {
          float: left;
          width: 32%;
          height: 192px;
          text-align: center;
          margin-right: 1.5%;
          padding: 26px 26px 0 26px;          
          background-color: #fff;
          border-radius: 1px;
          img {
            width: 100%;
            margin-bottom: 20px;
          }
          .name {
            font-size: 16px;
            line-height: 22px;
            color: #4E4C46;
          }
        }
        li:nth-child(3n + 3) {
          margin-right: 0;
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
</style>
