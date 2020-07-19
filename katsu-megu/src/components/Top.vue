<template lang="pug">
  div.pb-5
    v-layout(row wrap)
      v-flex(xs12)
        img(src="static/top/main.jpg")
    v-layout.pt-3.pb-3.bg.white--text(row wrap)
      v-flex(xs12)
        div.gv WeddingReception@DUO
        div.gv March 23th, 2018 11:00

</template>

<script>
export default {
  name: 'Top',
  data () {
    return {
    }
  }
}
</script>

<style scoped>
.bg {
  background-color: #242540;
  margin-top: -6px;
}

@font-face {
  font-family: 'gv';
  src: url('../../static/font/GreatVibesRegular.otf') format('opentype');
}
.gv {
  font-family: 'gv';
  font-size: 3rem;
}
@media (max-width:767px) {
  .gv {
    font-size: 2rem;
  }
}

img {
  max-width: 100%;
  max-height: 100%;
}
</style>
