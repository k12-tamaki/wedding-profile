<template lang="pug">
  div.content--box.content--bottom
    div
      div.title--text Message
        div.line
          v-divider(inset)

      v-row.mt-5(no-gutters)
        v-col(cols="12")
          div.bg
            div.content
              h1.pt-5 入籍のご報告
              h2.pt-5
                div この度、佐藤義隆、本間恵は
                div 入籍、結婚いたしました。
              h2.pt-3
                div 2人共、目立つ事を苦手とし、
                div 歳も歳なので(笑)
              h2.pt-3
                div こういう形でお世話になった方々に
                div 報告させて頂く事になりました。
              h2.pt-3
                div 既に一緒に暮らし始めて半年。
                div 毎日2人と猫1匹で楽しく過ごしています。
              h2.pt-3
                div 今後も変わらず皆様と
                div お付き合いさせていただき、
              h2.pt-3
                div 新しく家族になった2人を
                div 見守っていただければ幸いです。
              h2.footer 2020年 吉日 佐藤義隆 佐藤恵
</template>

<script>
export default {
  name: 'Message',
  components: {},
  data() {
    return {}
  },
  methods: {}
}
</script>

<style scoped>
.bg {
  background: url('~@/static/message/backimage.jpg') no-repeat center;
  -webkit-background-size: cover;
  background-size: cover;
  background-position: center;
  position: relative;
  height: 100vh;
  min-height: 750px;
}
.bg::before {
  background-color: rgba(0, 0, 0, 0.6);
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  content: ' ';
}

.content {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
}
.content h1 {
  color: #fff;
  font-size: 3rem;
}
.content h2 {
  color: #fff;
  font-size: 1.8rem;
}
.content h2.footer {
  padding-right: 5%;
  text-align: right;
  position: absolute;
  bottom: 4%;
  width: 100%;
}

@media (max-width: 767px) {
  .bg {
    min-height: 600px;
  }
  .content h1 {
    font-size: 1.8rem;
  }
  .content h2 {
    font-size: 1.1rem;
  }
}
</style>
