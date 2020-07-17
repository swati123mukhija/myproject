<template>
  <div id="app">
    <h1>Fetch data with API</h1>
    <Cards/>
  </div>
</template>
<script>
import Cards from './components/card'
import Home from './components/home'
export default {
  name: 'App',
  components: {
    Cards
  }
};
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
 -webkit-font-smoothing: antialiased;
 -moz-osx-font-smoothing: grayscale;
 text-align: center;
 color: #2c3e50;
 margin-top: 60px;
}
@import'~bootstrap/dist/css/bootstrap.css'
</style>