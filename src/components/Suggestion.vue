<template>
        <div class="second" :key="suggestion.login.uuid" v-for="suggestion in this.suggestionData">
            <div class="pp" >
                    <img :src = "suggestion.picture.thumbnail"  class="side-img cursor-pointer"/>
                    <p>{{suggestion.name.first}} {{suggestion.name.last}} <br> <span>{{suggestion.name.first}}</span></p>
            </div>
            <p class="blue-text">Follow</p>
        </div>
</template>

<script>
export default {
    name: 'Suggestion',
    props: ['suggestionData'],

}
</script>

<style scoped>


    .second{
        display: flex;
        justify-content: space-between;
        margin: 3% 0;
    }


    .side-img{
        border-radius: 50%;
        width: 30px;
        height: 30px;
        font-size: 1.5rem;
        margin: auto 0;
    }
    /* .side-img:hover{
      color:green;

    } */

    .pp{
        display: flex;

    }

    .pp p{
        margin: auto 0;
        margin-left: 7px;
    }

    span{
      color: grey;
    }
    .blue-text{
        color: rgb(46, 199, 250);
        margin: auto 0;
    }
</style>
