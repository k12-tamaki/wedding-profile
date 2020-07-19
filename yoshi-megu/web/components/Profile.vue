<template lang="pug">
  div.content--box.content--bottom
    div
      div.title--text Profile
        div.line
          v-divider

      v-row.mt-5(no-gutters)
        v-col(cols="4" offset="1")
          img.icon--img(src="../static/profile/groom.png")
        v-col(cols="4" offset="2")
          img.icon--img(src="../static/profile/bride.png")

      v-row.mt-5(no-gutters)
        v-col.answer(cols="4") Yoshitaka
        v-col.question(cols="4") Name
        v-col.answer(cols="4") Megumi

      v-row.mt-5(no-gutters)
        v-col.answer(cols="4") 1972年5月9日
        v-col.question(cols="4") BirthDay
        v-col.answer(cols="4") 1981年5月2日

      v-row.mt-5(no-gutters)
        v-col.answer(cols="4") A型
        v-col.question(cols="4") Blood Type
        v-col.answer(cols="4") B型

      v-row.mt-5(no-gutters)
        v-col.answer(cols="4") 会社員 営業
        v-col.question(cols="4") Job
        v-col.answer(cols="4") ブライダル衣装

      v-row.mt-5(no-gutters)
        v-col.answer(cols="4") サーフィン、スノーボード
        v-col.question(cols="4") Hobby
        v-col.answer(cols="4") サーフィン、スノーボード、登山

      v-row.mt-5(no-gutters)
        v-col.answer(cols="4") 猫
        v-col.question(cols="4") Animal
        v-col.answer(cols="4") 猫

</template>

<script>
export default {
  name: 'Profile',
  data() {
    return {}
  }
}
</script>

<style scoped>
img.icon--img {
  max-width: 300px;
  width: 100%;
  max-height: 100%;
}

.question,
.answer {
  font-size: 1.5rem;
  min-height: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.question {
  font-weight: bold;
  border-bottom: solid 2px #242540;
}
.answer {
  border-bottom: solid 2px #fafafa;
}

@media (max-width: 767px) {
  .answer,
  .question {
    font-size: 0.8rem;
    min-height: 2rem;
  }
}
</style>
