<template>
  <div id="app">
    <div class="container text-center">
      <h1>ciaone</h1>
      <Disco 
        v-for= "(disco,index) in dischi"
        :key= "index"
        :disco= "disco"
      />
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import Disco from '@/components/Disco.vue'

export default {
  name: 'App',
  components: {
    Disco,
  },
  data(){
    return{
      axios,
      dischi:[]
    }
  },
  created (){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(res=>{
      /* console.log(res.data.response) */
      this.dischi= res.data

      console.log(this.dischi)
    })
    .catch(err=>{
      console.log(err)
    })
  }
}
</script>

<style lang="scss">
@import '@/assets/style/general';
</style>
