<template>
  <v-app>
    <Navbar/>

    <v-content>
      <LandingPage/>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar'
import LandingPage from './components/LandingPage'

export default {
  name: 'App',
  components: {
    Navbar,
    LandingPage
  },
  data () {
    return {
      //
    }
  }
}
</script>
