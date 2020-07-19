<template lang="pug">
  div(id="app")
    div(v-scroll="onScroll")
      div.header
        v-tabs(
          slot="extension"
          v-model="tab"
          color="#242540"
          grow
        )
          v-tabs-slider(color="white")
          v-tab(
            v-for="item in items"
            :key="item"
            @click.stop="onClickTab(item)"
          )
            span.white--text {{item}}

      Top(id="Top")
      Profile.pt-5(id="Profile")
      Photo.pt-5(id="Photo")
      Food.pt-5(id="Food")
      Access.pt-5(id="Access")
      //- Contact.pt-5(id="Contact")

    div.footer.white--text Created by Katsunari
</template>

<script>
import Top from './components/Top'
import Profile from './components/Profile'
import Photo from './components/Photo'
import Food from './components/Food'
import Access from './components/Access'
import Contact from './components/Contact'

export default {
  name: 'App',
  components: {
    Top,
    Profile,
    Photo,
    Food,
    Access,
    Contact
  },
  data () {
    return {
      offsetTop: 0,
      tab: null,
      items: [
        'Top',
        'Profile',
        'Photo',
        'Food',
        'Access'
      ]
    }
  },
  methods: {
    onClickTab (item) {
      const options = {
        duration: 300,
        offset: 0,
        easing: 'easeInOutCubic'
      }
      let target = 0
      if (item !== 'Top') {
        target = '#' + item
      }
      this.$vuetify.goTo(target, options)
    },
    onScroll () {
      this.scrollEvent('Top')
      this.scrollEvent('Profile')
      this.scrollEvent('Photo')
      this.scrollEvent('Food')
      this.scrollEvent('Access')
      // this.scrollEvent('Contact')
    },
    scrollEvent (id) {
      const target = document.getElementById(id)
      var targetTop = target.getBoundingClientRect().top
      var targetBottom = target.getBoundingClientRect().bottom

      if (targetTop < 20 || window.innerHeight >= targetBottom) {
        const index = this.items.indexOf(id)
        this.tab = index
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /*margin-top: 60px;*/
}

.header {
  position: sticky; /* スクロールしても固定表示したい */
  top: 0; /* 画面上部の位置で固定 */
}

.footer {
  font-size: 1.2rem;
  background-color: #242540;
  vertical-align: middle;
  height: 70px;
  line-height: 70px;
}
</style>
