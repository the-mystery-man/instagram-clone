<template>
    <q-header elevated class="bg-white text-black header" >
      <q-toolbar >
        
        <q-toolbar-title class = "toolbar-title">
          Instagram
        </q-toolbar-title>

        <q-input standout v-model="text" placeholder="Search" :dense="dense" style="width:320px" class="q-mr-xl">
            <template v-slot:prepend>
                <q-icon name="search" />
            </template>
        </q-input>

    

        <div class="q-pa-md q-gutter-sm" >
          <q-btn flat round icon="home" />
          <q-btn flat round icon="send" />
          <q-btn flat round  icon="add" />
          <q-btn flat round icon="explore" />
          <q-btn flat round icon="favorite_outline" />
        </div>
        <div class="profile">
            <q-icon name="person" class="profile-pic" />
        </div>
      </q-toolbar>
    </q-header>
    
</template>


<script>
export default {
    name:  "Navbar",
}
</script>

<style scoped>
    .profile-pic{
        width: 100%;
        font-size: 1.2rem;
        display: flex;
        align-content: center;
    }

    .profile{
        height: 25px;
        width: 25px;
        border-radius: 50%;
        border: 2px solid;
        margin-left: 0;
    }


    .toolbar-title {
        /* font-family: 'Billabong, cursive' */
    }
    .badguy:focus{
        background-color: none;
    }
    .header{
        padding: 0 15%;
        height: 70px;
    }
</style>