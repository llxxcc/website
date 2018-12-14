<template>
  <div class="header">
    <div class="logo">
      <nuxt-link :to="'/' + $store.state.locale">
        <img src="~/assets/imgs/goc.svg" alt="">
      </nuxt-link>
    </div>
    <ul class="menu">
      <li>
        <a style="color: #fff; text-decoration: none;" target="_blank" href="https://market.goc.network/">
          {{$t('GocToken.Header.menu1')}}
        </a>
      </li>
    </ul>
    <div class="language" @click.stop="toggleLangMenu">
      <img class="show-img" :src="require(`~/assets/imgs/${$store.state.locale}.png`)"/>
      <i class="el-icon-arrow-down"></i>
      <div class="language-menu" v-if="showLangMenu">
        <nuxt-link
          class="item"
          v-for="(v, k) in langMap"
          :to="'/' + v + url"
          :key="k">
          <img :src="require(`~/assets/imgs/${v}.png`)" alt="">
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    url: String
  },
  data() {
    return {
      loginDialog: false,
      langMap: ['en', 'zh'],
      showLangMenu: false
    }
  },
  created() {
    this.setLang()
  },
  mounted() {
    window.addEventListener('click', this.langHidden)
  },
  methods: {
    toggleLangMenu() {
      this.showLangMenu = !this.showLangMenu
    },
    setLang() {
      this.langView = this.langMap[this.$store.state.locale]
    },
    langHidden() {
      this.showLangMenu = false
    }
  }
}
</script>


<style lang="scss" scoped>
.header {
  padding: 0 30px;
  height: 50px;
  line-height: 50px;
  background-color: #272622;
  .logo {
    float: left;
    margin-top: 10px;
    line-height: 27px;
    a {
      img {
        width: 65px;
      }
    } 
  }
  .menu {
    float: left;
    list-style: none;
    color: #FFFBF4;
    margin-left: 30px;
    cursor: pointer;
    li:hover {
      color: rgba(255, 255, 255, .5);
    }
  }
  .language {
    position: relative;
    float: right;
    text-align: center;
    width: 100px;
    margin-left: 30px;
    cursor: pointer;
    .show-img {
      float: left;
      margin-top: 18px;
    }
    .el-icon-arrow-down {
      float: left;     
      margin-top: 24px;
      margin-left: 5px;
      border: 5px solid transparent;
      border-top-color: #fff;
    }
    .language-menu {
      width: 50px;
      position: absolute;
      top: 50px;
      right: 62px;
      background: rgba(255, 255, 255, .3);
      z-index: 1;
      .item {
        display: block;
        width: 100%;
        line-height: 40px;
        height: 40px;
        text-align: center;
        color: #000;
        text-decoration: none;
        cursor: pointer;
      }
    }
  }
}
</style>
