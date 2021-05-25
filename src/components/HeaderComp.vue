<template>
  <div>
    <!-- <h1>logo spotify</h1> -->
    <div class="logo ms-3">

    <img src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png" alt="logo spotify">
    </div>

  </div>
</template>

<script>
export default {
  name: "HeaderComp"
}
</script>

<style lang="scss" scoped>

div{
  
  height: 50px;
  background-color: #2E3A46;
  margin-bottom: 20px;
  align-items: center;

  .logo{
    display: flex;
  }

  img{
    width: 40px;
    height: 40px;
  }
  /* h1{
    color: white;
  } */
}


</style>