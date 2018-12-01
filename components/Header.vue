<template>
  <div class="header">
    <div class="container">
      <a href="#page1">
        <img @click="move(0)" src="~/assets/imgs/goc.svg" class="logo" alt="">
      </a>
      <div class="language" @click.stop="toggleLangMenu">
        <img class="show-img" :src="require(`~/assets/imgs/${$store.state.locale}.png`)"/>
        <i class="el-icon-arrow-down"></i>
        <div class="language-menu" v-if="showLangMenu">
          <nuxt-link
            class="item"
            v-for="(v, k) in langMap"
            :to="'/' + v"
            :key="k">
            <img :src="require(`~/assets/imgs/${v}.png`)" alt="">
          </nuxt-link>
        </div>
      </div>
      <ul class="anchor-list">
        <li
          v-for="(v, i) in anchors"
          :class="i === curr ? 'curr' : ''"
          @click="move(i)"
          :key="i">
          <a :href="`#page${i + 1}`">{{v}}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    page: Number
  },
  data() {
    return {
      anchors: [this.$t('Index.Header.anchor1'), this.$t('Index.Header.anchor2'), this.$t('Index.Header.anchor3'), this.$t('Index.Header.anchor4'), this.$t('Index.Header.anchor5')],
      curr: this.page,
      langMap: ['en', 'zh'],
      showLangMenu: false,
    }
  },
  created() {
    this.setLang()
  },
  mounted() {
    document.body.addEventListener('click', () => {
      this.showLangMenu = false
    })
  },
  methods: {
    move(page) {
      this.curr = page
    },
    toggleLangMenu(e) {
      this.showLangMenu = !this.showLangMenu
    },
    setLang() {
      this.langView = this.langMap[this.$store.state.locale]
    }
  },
  watch: {
    page: function (n, o) {
      this.curr = n
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 60px;
  z-index: 999;
  color: #fff;
  background: #0f0f11;
  .logo {
    float: left;
    width: 90px;
    margin-top: 8px;
    cursor: pointer;
  }
  .anchor-list {
    float: right;
    margin-top: 20px;
    list-style: none;
    li {
      float: left;
      font-size: 16px;
      line-height: 18px;
      font-weight: 500;
      letter-spacing: 0.19px;
      margin-right: 40px;
      cursor: pointer;
      a {
        color: #fff;
        text-decoration: none;
      }
      a:hover {
        color: #FFC100;
      }
    }
    li:last-child {
      margin-right: 0px;
    }
    li.curr {
      padding-bottom: 3px;
      border-bottom: 2px solid #FFC100;
      a {
        color: #FFC100;
      }
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
      margin-top: 22px;
    }
    .el-icon-arrow-down {
      float: left;     
      margin-top: 28px;
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

