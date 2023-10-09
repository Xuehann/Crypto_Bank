<template>
  <WelcomeCpp/>
  <AddCoin @added="change" />
  <ProfitDisplay :key="refreshComp"/>
</template>

<script>
import WelcomeCpp from '/Users/xuehan/Desktop/Exercise/classEx/src/components/WelcomeCpp.vue'
import AddCoin from '/Users/xuehan/Desktop/Exercise/classEx/src/components/AddCoin.vue'
import ProfitDisplay from '/Users/xuehan/Desktop/Exercise/classEx/src/components/ProfitDisplay.vue'

export default {
  name: 'App', 
  components:{
    WelcomeCpp,
    ProfitDisplay,
    AddCoin,
  },
  data(){
    return{
      refreshComp:0
    }
  },

  methods:{
    change(){
      this.refreshComp +=1
    }
}}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-sommthing: grayscale;
  text-align: center;
  color:#2c3e50;
  margin-top:30px;
}

#bg {
  display: block;
  margin-left: auto;
  margin-right:auto;
  width: 60%;
}
</style>