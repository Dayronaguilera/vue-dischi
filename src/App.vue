<template>
  <div id="app">
    <Header />
    <Main :albums="albums" /> <!--in questo casa mandiamo il nostro array nel main -->
    
  </div>
</template>

<script>
import axios from 'axios'; //importiamo axios per poter fare le chiamate API
import Header from '@/components/Header.vue'; //importiamo header
import Main from '@/components/Main.vue'; //importiamo main

export default {
  name: 'App',
  components: {
    Header,
    Main, 
  },
   data() {
    return { //mettiamo return cosi ci restituisce un array da poter richiamare altrove
      albums:[], //creiamo un array che si popolera con la nostra chiamata api
    }
  },
  created() { //facciamo la nostra chiamata Api
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.albums = result.data.response //(element).data.(array che ci serve)
    })
  }
}
</script>

<style lang="scss">

</style>
