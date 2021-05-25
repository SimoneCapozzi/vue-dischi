<template>
  <div>
    <!-- <h1>Generi</h1> -->
    <select class="form-select" aria-label="Default select example">
      <option selected>Select Genre</option>
      <option value="1">Jazz</option>
      <option value="2">Rock</option>
      <option value="3">Pop</option>
      <option value="4">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: 'Search'
}
</script>

<style lang="scss" scoped>

div{
  display: flex;
  justify-content: center;
  margin: auto;
  height: 50px;
  width: 200px;
  background-color: aquamarine;
  margin-bottom: 20px;
}

</style>