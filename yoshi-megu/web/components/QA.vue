<template lang="pug">
  div.content--box.content--bottom
    div
      div.title--text Beginning
        div.line
          v-divider

      v-row.mt-5(no-gutters align="center")
        v-col(cols="12")
          v-list.qa--content(color="transparent")
            v-list-group.question--content(
              v-for="item in items"
              :key="item.title"
              v-model="item.active"
              no-action=""
              active-class="question--content--active"
            )
              template(v-slot:activator="")
                v-list-item-content
                  v-list-item-title.question--item.ptb--08 {{item.question}}
              v-list-item.answer--item.ptb--08(no-action)
                div
                  p(v-for="answer in item.answer") {{answer}}

</template>

<script>
export default {
  name: 'Beginning',
  components: {},
  data() {
    return {
      items: [
        {
          question: '2人の出会いは？',
          answer: [
            '2人の出会いは友人の紹介。',
            '共通の友人で僕の友人の奥さん。かたや、恵さんと同じ職場で働いてるという関係です。',
            'まずは友人として紹介され、共通の趣味のスノーボードに行き始めたのがきっかけでした。'
          ]
        },
        {
          question: 'プロポーズの言葉は？',
          answer: ['元旦、雪山で「今年結婚しよう」と指輪を渡しました。']
        },
        {
          question: '住まいは？',
          answer: ['変わらず富里市に住んでいます！']
        }
      ]
    }
  },
  methods: {}
}
</script>

<style scoped>
.qa--content {
  border-top: 1px solid #1b2538;
  border-color: #1b2538 !important;
  padding: 0;
}
.question--content {
  border-bottom: 1px solid #1b2538;
}
.question--item {
  font-size: 1.2rem;
  font-weight: bold;
  color: #1b2538;
}
.question--content--active .question--item {
  color: #00838f;
}

.answer--item {
  padding-left: 1rem !important;
  text-align: left;
  background: rgba(0, 131, 143, 0.5);
}
.answer--item p {
  color: #ffffff;
  font-size: 1.1rem;
  font-weight: bold;
}
@media (max-width: 767px) {
  .answer--item p {
    font-size: 1rem;
  }
}

.ptb--08 {
  padding-top: 0.8rem;
  padding-bottom: 0.8rem;
}
</style>
