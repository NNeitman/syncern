<template>
  <OnboardingFlow style="max-width:600px; margin: 0 auto;"/>
</template>

<script>
import 'primeflex/primeflex.css';
import OnboardingFlow from './components/Onboarding/OnboardingFlow'

export default {
  name: 'App',
  components: {
    OnboardingFlow
  },
  methods: {
    handlePlay: function (event) {
      console.log(30)
      console.log(event)
    },
    handlePause: function (event) {
      console.log(30)
      console.log(event)
    },
    handleBufferLocationChange: function (event) {
      console.log(30)
      console.log(event)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<style src="primevue/resources/themes/saga-blue/theme.css"></style>
<style src="primevue/resources/primevue.min.css"></style>
<style src="primeicons/primeicons.css"></style>

