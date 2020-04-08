<template>
  
 <div class="container">
  <div class="row max-height align-items-center">
   <div class="col-10 col-md-6 mx-auto text-center">
    <h1 class=text-uppercase>hex color :<span id="hex-value">{{value}}</span></h1>
    <a href="#" id="btn" class="btn btn-secondary text-uppercase my-2" v-on:click="changeHex()">click me</a>
   </div>
  </div>
 </div>
</template>

<script>
export default {
  
  data () {
    return {
   hexValues:[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 'A', 'B', 'C', 'D', 'E', 'F'],
   value:''
    }
  }, 
  methods:{
    changeHex(){
      let hex = '#'

      for(let i = 0; i< 6; i++){
        const index = Math.floor(Math.random()* this.hexValues.length)

        hex+= this.hexValues[index]
      }
      this.value = hex;
      document.body.style.backgroundColor = hex;
    }
  }
}
</script>

<style>
.max-height{
 min-height: 100vh;
}
</style>
