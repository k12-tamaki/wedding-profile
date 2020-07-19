<template lang="pug">
  div.bg.pb-5.white--text
    p
      v-layout(row wrap)
        v-flex(xs12)
          div.gv Contact
          div.line
            v-divider(dark)

      v-layout.main(row wrap)
        v-flex(xs6)
          div.item Katsunari
          div.mt-3
            v-btn(fab dark color="cyan" @click="onClickTel('09083132026')")
              v-icon phone
            v-btn(fab dark color="cyan" @click="onClickMail('k12.tamaki@gmail.com')")
              v-icon mail
        v-flex(xs6)
          div.item Megumi
          div.mt-3
            v-btn(fab dark color="cyan" @click="onClickTel('08053795669')")
              v-icon phone
            v-btn(fab dark color="cyan" @click="onClickMail('tkk91x@gmail.com')")
              v-icon mail
</template>

<script>
export default {
  name: 'Contact',
  data () {
    return {
    }
  },
  methods: {
    onClickTel (tel) {
      location.href = 'tel:' + tel
    },
    onClickMail (mail) {
      location.href = 'mailto:' + mail
    }
  }
}
</script>

<style scoped>
.bg {
  background-color: #242540;
}
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
div.item {
  font-size: 1.5rem;
}
@media (max-width:767px) {
  .gv {
    font-size: 4rem;
  }
  .line {
    width: 50px;
  }
  div.item {
    font-size: 1rem;
  }
}
</style>
