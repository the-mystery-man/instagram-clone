<template>
  <q-layout view="lHh Lpr lFf">
    <p>Just testing to see if logging in to a different account actually worked.</p>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>

import { defineComponent } from 'vue'

export default defineComponent({
  name: 'MainLayout',

})
</script>
