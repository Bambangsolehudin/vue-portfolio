<template>
  <div class="App">
    <Home v-if="isHome" @showNotif="showNotif" />

    <Notif v-if="!isHome" @backHome="showHome" />
  </div>
</template>

<script>
import Home from '@/components/home/home.vue'
import Notif from '@/components/notification/notif.vue'


export default {
  components: {
    Home, Notif
  },
  data() {
    return {
      isHome: true
    }
  },

  methods: {
    showNotif() {
      this.isHome = false
    },
    showHome(){
      this.isHome = true
    }
  },
}
</script>

<style>

</style>