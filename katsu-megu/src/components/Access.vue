<template lang="pug">
  div.pb-5
    v-layout(row wrap)
      v-flex(xs12)
        div.gv Access
        div.line
          v-divider

    v-layout.main(row wrap)
      v-flex(xs12)
        p.name
          a(
            href="https://www.duo-gc.com/sp/"
            target="_blank"
          ) ブライダルステージデュオ・グランシャリオ
    v-layout(row wrap)
      v-flex(xs12)
        p
          div.address 〒950-0982
          div.address 新潟市中央区堀之内南3丁目7番10号
    v-layout(row wrap)
      v-flex(xs12)
        p
          div.access-title ■お車でお越しの場合
          div.access-detail
            div.text-xs-left 新潟バイパス 桜木ICより 約3分
            div.text-xs-left 北陸自動車道 新潟西ICより 約20分
            div.text-xs-left 磐越自動車道 新潟中央ICより 約15分
        p
          div.access-title ■新潟駅より
          div.access-detail
            div.text-xs-left タクシー：新潟駅南口より 約7分
    v-layout(row wrap)
      v-flex(xs12)
        v-btn.white--text(
            color="cyan"
            @click.stop="openMap"
          ) Google Mapで開く

</template>

<script>
export default {
  name: 'Access',
  data () {
    return {
    }
  },
  methods: {
    openMap () {
      open('https://www.google.co.jp/maps/search/%E3%83%96%E3%83%A9%E3%82%A4%E3%83%80%E3%83%AB%E3%82%B9%E3%83%86%E3%83%BC%E3%82%B8+%E3%83%87%E3%83%A5%E3%82%AA/@37.9027045,139.0467922,17z/data=!3m1!4b1?hl=ja')
    }
  }
}
</script>

<style scoped>
@font-face {
  font-family: 'gv';
  src: url('../../static/font/GreatVibesRegular.otf') format('opentype');
}
.gv {
  font-family: 'gv';
  font-size: 8rem;
}
.line {
  width: 100px;
  margin: auto;
}
.main {
  margin-top: 80px;
}

.name {
  font-size: 1.8rem;
}
.address {
  font-size: 1.6rem;
}
.access-title {
  font-size: 1.4rem;
}
.access-detail {
    width: 300px;
    margin: auto;
  }
  .access-detail div {
    font-size: 1.2rem;
  }

@media (max-width:767px) {
  .gv {
    font-size: 4rem;
  }
  .line {
    width: 50px;
  }
  .name {
    font-size: 1.1rem;
  }
  .address {
    font-size: 1rem;
  }
  .access-title {
    font-size: 1rem;
  }
  .access-detail {
    width: 250px;
    margin: auto;
  }
  .access-detail div {
    font-size: 1rem;
  }
}
</style>
