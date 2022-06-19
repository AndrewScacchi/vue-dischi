<template>
    <div id="header">
        <img id="logoSmall" src="../assets/img/Spotify_logo.svg" alt="">
    </div>
</template>

<script>

export default {
  name: 'MyHeader',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  #header {
    width: 100%;
    height: 50px;
    background-color: #2e3a46;

    #logoSmall{
      width: 35px;
      margin: 7.5px 10px;
    }
  
  }
</style>
