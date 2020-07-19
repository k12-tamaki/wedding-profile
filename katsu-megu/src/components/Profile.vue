<template lang="pug">
  div.pb-5
    v-layout(row wrap)
      v-flex(xs12)
        div.gv Profile
        div.line
          v-divider

    v-layout.mt-5(row wrap)
      v-flex(xs4 offset-xs1)
        img(src="static/profile/katsu.jpg")
      v-flex(xs4 offset-xs2)
        img(src="static/profile/megu.jpg")

    v-layout.mt-5(row wrap)
      v-flex(xs4)
        div.prof-text.answer
          div 田巻 勝成
          div 1989年2月21日
          div A型
          div SE
          div ゲーム
          div カレー
          div
            a(href="https://www.suntory.co.jp/whisky/yamazaki/" target="_blank") 山崎
          div
            a(href="http://www.ramen-walker.com/shop_58.html" target="_blank") 心一家
            span 、
            a(href="https://tabelog.com/niigata/A1501/A150101/15009289/" target="_blank") 揚子江

      v-flex(xs4)
        div.prof-text.question
          div Name
          div BirthDay
          div Blood Type
          div Job
          div Hobby
          div Food
          div Liquor
          div Ramen

      v-flex(xs4)
        div.prof-text.answer
          div 髙木 萌
          div 1989年8月4日
          div AB型
          div SE
          div マンガ
          div コロッケ
          div
            a(href="https://www.kikusui-sake.com/home/jp/products/p019/" target="_blank") 五郎八
          div
            a(href="http://www.ramen-walker.com/shop_21.html" target="_blank") しゃがら

</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
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
.prof-text div {
  font-size: 1.5rem;
  height: 3rem;
  line-height: 3rem;
}
@media (max-width:767px) {
  .gv {
    font-size: 4rem;
  }
  .line {
    width: 50px;
  }
  .prof-text div {
    font-size: 1rem;
    height: 2rem;
    line-height: 2rem;
  }
}

.main {
  margin-top: 80px;
}
.prof-text.question div {
  border-bottom: solid 2px #242540;
}
.prof-text.answer div {
  border-bottom: solid 2px #ffffff;
}
img {
  max-width: 300px;
  width: 100%;
  max-height: 100%;
}
</style>
