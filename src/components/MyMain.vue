<template>
    <div id="main">
      <div id="container">

      </div>
        
    </div>
</template>

<script>
export default {
  name: 'MyMain',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  #main {
    width: 100%;
    height: calc(100vh - 50px);
    background-color: #1e2d3b;
    padding: 25px 0;
  }
  #container{
    width: 80%;
    margin: 0 auto;
    border: 1px solid red;
    min-height: 400px;
  }
</style>
