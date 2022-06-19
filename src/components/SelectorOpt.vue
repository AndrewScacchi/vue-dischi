<template>
    <div>
        
        <select name="genre"
        v-model="inputGenere"
        @change="selectGenreList()"
        >
            <option value="all">All</option>
            <option value="pop">Pop</option>
            <option value="rock">Rock</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>

        
        
    </div>
</template>

<script>



export default {
    name: 'SelectorOpt',

    data(){
        return {
            inputGenere : "",
        }
    },

    methods: { 
        selectGenreList() {
            this.$emit('mySearch', this.inputGenere);
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
