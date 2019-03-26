<template>
  <div>
    <the-menu />
    <the-header />
    <Main />
    <the-footer />
  </div>
</template>

<script>
import TheMenu from '@/components/TheMenu.vue'
import TheHeader from '@/components/TheHeader.vue'
import TheFooter from '@/components/TheFooter.vue'
import Main from '@/layouts/Main.vue'

export default {
  name: 'Home',
  components: {
    TheMenu,
    TheHeader,
    TheFooter,
    Main
  }
}
</script>

