<template>
  <div>
    <Header/>
    <Main/>
    <Footer/>

  </div>
</template>

<script>
import axios from "axios";
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';




export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  created: function(){
    this.getApiList();

  },
  methods:{
    getApiList(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((result) =>{
        console.table(result.data.response);

      })
      .catch((error) =>{
        console.error(error)
      })
    }


  }

}
</script>

<style lang="scss">
@import '@/style/main-style.scss'

</style>
