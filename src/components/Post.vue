<template>
    <div class = "post-container">
        <!-- Post header -->
        <div class="post-header">
            <div class="row">
                <div class="col-1">
                    <q-btn round>
                        <q-avatar size = "40px">
                            <img :src = "this.post.picture.thumbnail" />
                        </q-avatar>
                    </q-btn>
                </div>
                <div class="col-11 side-to-avatar">
                    <div class = ''>
                        <div class="handle text-bold">{{ (this.post.name.first+ this.post.name.last).toLowerCase() }}</div>
                        <div class="under-handle">{{ this.post.location.city+", "+ this.post.location.state }}</div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Post Image -->
        <div class="post-image">
            <img @dblclick="likePost" :src = "this.post.picture.large" class = "post-image" />
            <div class="like-big">
                <q-icon v-show="this.showHeart" id="first" color="white" class = "big-boys" name ="favorite" />
            </div>
            
        </div>
        <!-- Post Footer -->
        <div class="post-footer">
            <div class="row q-mx-md">
                <div class="col-8 text-start icons-container">
                    <span v-if="postLiked">
                        <q-icon @click = "likePost" color="black" class = "post-icons  like-icons" name = "favorite_bordered" />  &nbsp;
                    </span>
                    <span v-else>
                        <q-icon v-show="this.postLiked" @click = "likePost" color="red" class = "post-icons " name ="favorite" />
                    </span>
                     <q-icon color = "black" class = "post-icons" name="chat_bubble_outline" />
                </div>
                <div class="col-4 text-end move-end">
                    <q-icon color = "black" class = "post-icons" name="bookmark_outline" />
                </div>
            </div>

            <div class="row stupid">
                <b> {{likes}} likes </b>
            </div>
            <div class="row">
                <div class="handle text-siz view-commentse"><b>{{ (this.post.name.first+ this.post.name.last).toLowerCase() }} </b> Lorem ipsum dolor, sit amet consectetur adipisicing elit. Expedita, recusandae consectetur voluptate pariatur similique voluptas quasi sit labore quisquam neque!</div>
            </div>
            <div class="row">
                <span @click = "toggleModal" class="text-muted view-comments">View all comments</span>
                <!-- <q-modal
                    v-model = "modalOpened"
                >
                    <h1>Quasar Modal</h1>
                </q-modal> -->
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:[ 'post' ],
    data(){
        return{
            postLiked: false,
            likes: Math.floor(Math.random() * 1000),
        }
    },
    methods: {
        showHeartFunc(){
            if(this.postLiked){
                this.showHeart = true;
                setTimeout(()=>{
                    this.showHeart = false;
                }, 300)
            }
        },
        likePost(){
            this.likes+=this.postLiked?-1:1;
            this.postLiked = !this.postLiked;
            this.likes+= this.postLiked ? 0 : 1;
        }
    }
}

</script>

<style scoped>
    .post-container{
        margin: 20px 0;
        border: 1px solid #ccc;
    }
    .post-header{
        margin: 20px
    }
    .text-bold{
        font-weight: bold
    }
    .side-to-avatar{
        padding-left: 10px 
    }
    .post-image{
        width: 100%;
        height: auto;
        position: relative;
    }
    .post-footer{
        margin: 20px
    }

    
    

    .bad{
        display: flex;
        width: 100%;
    }

    .badguy{
        position: relative;
    }

    .red-like{
        position: relative;
        left: 0;
    }

    .move-end{
        justify-content: flex-end;
    }
   

    .big-boys{
        font-size: 7.5rem;
        transition: display 300ms ease 300ms;
    }

    .like-big{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
    
    .post-icons{
        font-size: 190%;
    }
    .text-muted{
        color: #777;
        font-size: 80%
    }
    .text-size{
        font-size: 90%
    }
    .view-comments{
        cursor: pointer;
    }

</style>