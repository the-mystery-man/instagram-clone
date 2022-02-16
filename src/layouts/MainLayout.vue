<template>
  <q-layout view="lHh Lpr lFf">
    <Navbar />
    <Sidebar />

    <q-page-container class = "row justify-center">
      <div class = " inner-container" >
        <router-view />
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>

import { defineComponent } from 'vue'
import Navbar from '../components/Navbar'
import Sidebar from '../components/Sidebar'

export default defineComponent({
  name: 'MainLayout',
  components:{
    Navbar,
    Sidebar
  }
})
</script>


<style scoped>
.container{
  width: 80%;
  display: flex;
  justify-content: center;
}
.inner-container{
  width: 70%
}
/* @media only screen and ( max-width: 991px ){
  .container{
    width: 90%;
  }
}

@media only screen and ( min-width:  ) */
</style>