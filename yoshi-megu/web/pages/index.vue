<template lang="pug">
  div.index--content.normal-font
    Top(id="Top")
    Message(id="Message")
    Profile(id="Profile")
    QA(id="Beginning")
    Photo(id="Photo")
</template>

<script>
import Top from '~/components/Top.vue'
import Profile from '~/components/Profile.vue'
import QA from '~/components/QA.vue'
import Photo from '~/components/Photo.vue'
import Message from '~/components/Message.vue'

export default {
  components: {
    Top,
    Profile,
    QA,
    Photo,
    Message
  },
  data() {
    return {}
  },
  methods: {}
}
</script>

<style scoped>
.index--content > div:not(#Top) {
  z-index: 2;
  position: relative;
  background-color: #fafafa;
}
</style>
