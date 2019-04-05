<template>
    <div id="app">
    <Calcula/>
    </div>
</template>

<script>
import Calcula from './components/Calcula.vue'
export default {
  name: 'app',
  components: {
    Calcula
  }
}
</script>

<style lang="scss">
    @import '../node_modules/bootstrap/scss/bootstrap.scss';
    #app{
      margin-top: 10px
    }
</style>
