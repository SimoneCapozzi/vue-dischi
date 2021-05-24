<template>

  <div class= "colonna-dischi col-sm-6 col-md-4 col-lg-5  text-center">

    <div class="block">
      <img class="img-fluid figur-img" :src="disco.poster" :alt="disco.title">
      <h4> {{ disco.title }} </h4>
      <h5> {{ disco.author}}</h5>
      <h5> {{ disco.year}}</h5>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Disco',
  props:{
    disco:Object
  }
}
</script>

<style lang="scss" scoped>
.block{
  height: 500px;
  background-color: #2E3A46;
  margin-bottom: 50px;
  
  img{
    /* width: 200px;
    height: 200px; */
    padding: 15px;
    
  }

  h4{
    margin-top: 20px;
    color: white;
    font-size: 30px;
    margin-bottom: 30px;
  }
  
  h5{
    color: #78726C;
  }
    
}

.col-lg-5{
  position: relative;
  min-height: 1px;
  padding-right: 15px;
  padding-left: 15px;
}

@media (min-width:1000px){
  .col-lg-5 {
    width: 20%;
    float: left;
  }
}

</style>