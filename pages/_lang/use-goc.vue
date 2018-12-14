<template>
  <section>
    <Header :url="'/use-goc'"></Header>
    <div class="index">
      <div class="kv">
        <div class="content">
          <span class="title">{{$t('GocToken.Kv.title')}}</span>
          <!-- <p>{{$t('GocToken.Kv.p1')}}</p> -->
          <!-- <p>{{$t('GocToken.Kv.p2')}}</p> -->
        </div>
        <img v-if="$store.state.locale === 'zh'" width="100%" src="~/assets/landingImgs/kv.jpg" alt="">
        <img v-else width="100%" src="~/assets/landingImgs/kv-en.jpg" alt="">
      </div>
      <div class="use-box">
        <div class="content">
          <span class="title">
            {{$t('GocToken.Use.title')}}
          </span>
          <p>{{$t('GocToken.Use.p1')}}</p>
          <p>
            {{$t('GocToken.Use.p2')}}
            <!-- <span class="address">TQiPS3ibWQ9XfsP3EVJs7pJzGRCzxzLeET</span> -->
          </p>
          <p>
            {{$t('GocToken.Use.p3')}}
            <!-- <span class="address">TMFthG5KtTUwfTnE93Ap4rCvMnTuGjUw1p</span> -->
          </p>
          <p>
            {{$t('GocToken.Use.p4')}}
            <!-- <span class="address"></span> -->
          </p>
          <p>{{$t('GocToken.Use.p5')}}</p>
          <p>{{$t('GocToken.Use.p6')}}</p>
        </div>
      </div>
      <!-- <div class="value">
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
          <p>{{$t('GocToken.Value.ps')}}</p>
          <p>{{$t('GocToken.Value.ps1')}}</p>
          <p>{{$t('GocToken.Value.ps2')}}</p>
          <p>{{$t('GocToken.Value.ps3')}}</p>
          <table>
            <thead>
              <tr>
                <th>{{$t('GocToken.Value.th1')}}</th>
                <th>{{$t('GocToken.Value.th2')}}</th>
                <th>{{$t('GocToken.Value.th3')}}</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(v, i) in list" :key="i">
                <td>{{v.address}}</td>
                <td>
                  {{$store.state.locale === 'en' ? v.num / 10 : v.num}}
                  {{$t('GocToken.Value.unit')}}
                </td>
                <td>{{v.owner}}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div> -->
      <div class="use-box value">
        <div class="content">
          <span class="title">
            {{$t('GocToken.Value.title')}}
          </span>
          <p>{{$t('GocToken.Value.p1')}}</p>
          <p>{{$t('GocToken.Value.p2')}}</p>
          <p>{{$t('GocToken.Value.p3')}}</p>
          <p class="small">{{$t('GocToken.Value.ps')}}</p>
          <p class="small" style="text-indent: 20px;">{{$t('GocToken.Value.ps1')}}</p>
          <p class="small" style="text-indent: 20px;">{{$t('GocToken.Value.ps2')}}</p>
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
        // {img: require('~/assets/landingImgs/icon5.png'), title: this.$t('GocToken.Value.item5-title'), text: this.$t('GocToken.Value.item5-text')}
      ],
      wallets: [
        {zh: require('~/assets/landingImgs/itron.png'), en: require('~/assets/landingImgs/itron.png'), name: this.$t('GocToken.Wallet.item1-name')},
        {zh: require('~/assets/landingImgs/cobo.png'), en: require('~/assets/landingImgs/cobo.png'), name: this.$t('GocToken.Wallet.item2-name')},
        {zh: require('~/assets/landingImgs/math.png'), en: require('~/assets/landingImgs/math-en.png'), name: this.$t('GocToken.Wallet.item3-name')}
      ],
      list: [
        {address: 'TQiPS3ibWQ9XfsP3EVJs7pJzGRCzxzLeET', num: '30', owner: 'GOC foundation'},
        {address: 'TMFthG5KtTUwfTnE93Ap4rCvMnTuGjUw1p', num: '10', owner: 'GOC token fund'},
        {address: 'TRfPZzCZLUcfZ6cJLyrcGBRwgXyQoQuBkL', num: '20', owner: 'GOC ' + this.$t('GocToken.Value.teamExcitation')},
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
      p:nth-child(2) {
        font-size: 18px;
        font-weight: 600;
        line-height: 56px;
      }
      p:last-child {
        margin-top: 20px;
      }
      .address {
        display: inline-block;
        padding-left: 30px;
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
    // .content {
    //   overflow: hidden;
    //   width: 1100px;
    //   margin: 0 auto;
    //   padding: 60px 0;
    //   .title {
    //     width: 100%;
    //     text-align: center;
    //     font-size: 30px;
    //     color: #4E4C46;
    //     margin-bottom: 50px;
    //   }
    //   > ul {
    //     list-style: none;
    //     width: 100%;
    //     li {
    //       float: left;
    //       width: 32%;
    //       height: 370px;
    //       text-align: center;
    //       margin-right: 1.5%;
    //       padding: 20px 32px 0 32px;          
    //       background-color: #f3f3f3;
    //       border-radius: 1px;
    //       margin-bottom: 28px;
    //       img {
    //         width: 160px;
    //       }
    //       .item-title {
    //         font-size: 18px;
    //         color: #4E4C46;
    //         margin-bottom: 17px;
    //       }
    //       .item-text {
    //         text-align: left;
    //         width: 100%;
    //         font-size: 15px;
    //         line-height: 21px;
    //         color: #97948F;
    //       }
    //     }
    //     li:nth-child(3n + 3) {
    //       margin-right: 0;
    //     }
    //     .lengthen {
    //       height: 420px;
    //     }
    //   }
    //   > p {
    //     margin-left: 40px;
    //   }
    //   > table {
    //     margin: 10px 0 0 30px;
    //     th, td {
    //       padding: 4px 8px;
    //     }
    //     thead {
    //       tr {
    //         th:first-child {
    //           text-align: left;
    //         }
    //       }
    //     }
    //   }
    // }
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
