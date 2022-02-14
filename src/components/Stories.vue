<template>
    <div class = "flex row story-container">
        <div class = "story-item" :key = "userStory.login.uuid" v-for = "userStory in this.userStories">
            <Story class="" :userStory="userStory" />
        </div>
    </div>
</template>

<script>
import Story from './Story';

export default {
    name: "Stories",
    props: ['userStories'],
    components: {
        Story
    }
}
</script>

<style scoped>
    .stories-container{
        border: 1px solid #ccc;
        border-radius: 5px;
        overflow-x:scroll;
        overflow-y: hidden;
        height: 100px;
        width: 100%
    }
    .story-container{
        height: 100px;
        width: 100%;
        
        overflow-x: scroll;
        overflow-y: hidden;
        white-space: nowrap;
    }
    .inner-container{
        display: inline-block
    }
</style>