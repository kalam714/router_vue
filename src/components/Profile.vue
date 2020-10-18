<template>
  <div class="hello">
      <h1>Profile Page {{userId}}</h1>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
      userId :this.$route.params.getid
    }
  },
  methods:{
     updateId(){
       this.userId =  this.$route.params.getid
     }
  },
  watch:{
      $route:'updateId'
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1{
    color:aqua;
    text-align: center;
}
</style>
