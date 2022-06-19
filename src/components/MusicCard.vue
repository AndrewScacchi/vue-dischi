<template>
    <div class="card">
        <img :src="albumObj.poster" :alt="albumObj.title">
        <h3>{{albumObj.title}}</h3>
        <p>{{albumObj.author}}</p>
        <p>{{albumObj.year}}</p>
    </div>  
</template>

<script>
export default {
  name: 'MusicCard',
  props: {
    albumObj: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .card {
        width: 18%;
        background-color: #2e3a46;
        margin: 10px;
        padding: 15px 10px;
        text-align: center;

        img {
            width: 90%;
            height: 150px;
            object-fit: cover;
        }

        h3 {
            color: white;
            text-transform: uppercase;
        }

        p {
            color: gray;
        }
    }
</style>
