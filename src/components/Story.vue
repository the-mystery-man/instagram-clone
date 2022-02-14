<template>
    <div class = "story text-center">
        <div>
            <q-btn round class = "avatar-container">
                <q-avatar size = "60px">
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
        /* float: left; */
        display: inline-block;
    }
    .avatar-container{
        margin: 5px 10px;
    }
</style>