<template>
  <div id="app">
    <Box/>
    <p>
        a:<input type="number" v-model.number="a"><br/>
    </p>
    <p>
        b:<input type="number" v-model.number="b"><br/>
    </p>
    <p>
      求和：{{count}}
    </p>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>
<script>
import Box from './components/Box.vue'
export default {
  components:{
    Box
  },
  data(){
    return {
      a:0,
      b:0,
      message:'hello vue'
    }
  },
  computed:{
    count(){
      return this.a+this.b;
    }
  }
}
</script>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>


