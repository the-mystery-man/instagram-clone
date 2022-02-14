<template>
    <div class="main">
        <div class="side">
            <div class="side-profile">
                <div class="pp">
                    <q-icon name="person" class="side-img" />
                    <p>Lorem Dude <br> <span>Dude</span></p>
                </div>
                <p class="blue-text">Switch</p>
            </div>
        </div>
    <!-- Suggestion for you -->
        <div class="suggest">
            <p>Suggestion for You</p>
            <p>See All</p>
        </div>

        <Suggestion />


    </div>



</template>

<script>
import Suggestion from '../components/Suggestion'

export default {
    name: 'Sidebar',
    components:{
        Suggestion
    }
}
</script>

<style scoped>


    .main{
        width: 20%;
        position: fixed;
        top: 110px;
        right: 15.7%;
        height: 100vh;
        padding: 0.5%;
    }

    .side-profile{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-top: 10px;
    }

    .side-img{
        border: 1px solid;
        border-radius: 50%;
        width: 50px;
        height: 50px;
        font-size: 2.5rem;
         cursor: pointer !important;
    }

    .pp{
        display: flex;
    
    }

    .pp p{
        margin: auto 0;
        margin-left: 7px;
    }
    .blue-text{
        color: blue;
        margin: auto 0;
    }
    .suggest{
        display: flex;
        justify-content: space-between;
    }
    .suggest p{
        margin: 15px 0;
    }
</style>