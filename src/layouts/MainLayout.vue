<template>
  <q-layout view="lHh Lpr lFf">

    <q-page-container class = "row justify-center">
      <div class = " inner-container" >
        <router-view />
      </div>
    </q-page-container>
  </q-layout>
</template>

<script>

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MainLayout'
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