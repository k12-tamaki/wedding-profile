<template lang="pug">
  div.pb-5
    v-layout(row wrap)
      v-flex(xs12)
        div.gv Food
        div.line
          v-divider

    v-layout.main(row wrap)
      v-flex(xs12)
        div.comment.mb-3 お料理選択の参考にしてください
        img(src="static/food/choise1.png")
        img(src="static/food/choise2.png")
</template>

<script>
export default {
  name: 'Food',
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
.main {
  margin-top: 80px;
}
.comment {
  font-size: 1.5rem;
}
@media (max-width:767px) {
  .gv {
    font-size: 4rem;
  }
  .line {
    width: 50px;
  }
  .comment {
    font-size: 1rem;
  }
}

img {
  max-width: 100%;
  max-height: 100%;
}
</style>
