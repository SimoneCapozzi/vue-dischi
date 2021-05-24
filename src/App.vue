<template>
  <div id="app">

    <Loader 
    v-if= "loading === true"
    />

    <div
    v-else
    >

      <HeaderComp />

      <div class="container">
        <div class="row">


        <Disco 
          v-for= "(disco,index) in dischi"
          :key= "index"
          :disco= "disco"
          />
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import axios from 'axios'
import Disco from '@/components/Disco.vue'
import HeaderComp from '@/components/HeaderComp.vue'
import Loader from '@/components/Loader.vue'


export default {
  name: 'App',
  components: {
    Disco,
    HeaderComp,
    Loader,
  },
  data(){
    return{
      axios,
      dischi:[],
      loading:true,
    }
  },
  created (){
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(res=>{
      /* console.log(res.data.response) */
      this.dischi= res.data.response
      this.loading = false;
      /* console.log(this.dischi) */
    })
    .catch(err=>{
      console.log(err)
    })
  }
}
</script>

<style lang="scss">
@import '@/assets/style/general';

#app{
  background-color: #1E2D3B;

  .header{
    width: 100%;
    background-color: #2E3A46;
    margin-bottom: 20px;
  }
}
</style>
