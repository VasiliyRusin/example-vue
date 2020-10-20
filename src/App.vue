<template>
  <div id="app">
      <!--    <div id="nav">-->
      <!--      <router-link to="/">Home</router-link> |-->
      <!--      <router-link to="/about">About</router-link>-->
      <!--    </div>-->
      <!--    <router-view/>-->
    
    
      <Header :text.sync="text"></Header>
      <label>
          <input v-model="text">
      </label>
  </div>
</template>

<script>
    import Header from "@/components/Header";
    
    export default {
        name: "App",
        components: { Header },
        
        data () {
            return {
                text: ""
            };
        }
    };
</script>

<style lang="scss">
    #app {
        color: #2C3E50;
        text-align: center;
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }
    
    #nav {
        padding: 30px;
        
        a {
            font-weight: bold;
            color: #2C3E50;
            
            &.router-link-exact-active {
                color: #42B983;
    }
  }
}
</style>
