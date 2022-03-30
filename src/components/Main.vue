<template>
<div class="container-fluid">
    <div class="row row-cols-1 row-cols-md-3 g-4">
  <div class="col">
    <div class="card">
      <img src="" class="card-img-top" alt="">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
</div>
</div>
</template>

<script>
export default {
name: 'mainContent',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.row{
    border: 2px solid purple;
}
div.container-fluid{
background-color: rgb(77, 115, 153);
height:calc(100vh - 100px);
}
.card{
    width: 200px;
}
</style>
