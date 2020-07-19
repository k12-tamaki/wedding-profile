<template lang="pug">
  div.pb-5
    v-layout(row wrap)
      v-flex(xs12)
        div.gv Photo
        div.line
          v-divider

    v-layout.main(row wrap)
      v-flex(xs12)
        v-carousel(
          max="100%"
          height="100%"
        )
          v-carousel-item(
            v-for="(item,i) in items"
            :key="i"
            :src="item.src"
            reverse-transition="fade"
            transition="fade"
          )
</template>

<script>
export default {
  name: 'Photo',
  data () {
    return {
      items: [
        {
          src: '../../static/photo/img00.jpg'
        },
        {
          src: '../../static/photo/img01.jpg'
        },
        {
          src: '../../static/photo/img02.jpg'
        },
        {
          src: '../../static/photo/img03.jpg'
        },
        {
          src: '../../static/photo/img04.jpg'
        }
      ]
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
@media (max-width:767px) {
  .gv {
    font-size: 4rem;
  }
  .line {
    width: 50px;
  }
}
</style>
