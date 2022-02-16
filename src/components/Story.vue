<template>
    <div class = "story text-center">
        <div>
            <q-btn round class = "avatar-container ">
                <q-avatar size = "0px">
                    <img :src = "this.userStory.picture.thumbnail" />
                </q-avatar>
            </q-btn>
        </div>
        {{this.userStory.name.first.toLowerCase()}}
    </div>
</template>

<script>
export default {
    name: "Story",
    props: ['userStory']
}
</script>

<style scoped>
    .story{
        display: inline-block;
    }
    .avatar-container{
        margin: 5px 10px;
        background: linear-gradient(to right, rgb(206, 64, 64), rgb(128, 1, 60));
        padding: 2px
    }
</style>