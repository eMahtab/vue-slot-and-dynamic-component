<template>
  <div id="app">
   
   <div class="container">
        <div class="row">
            <div class="col-xs-12">
               
               <button class="btn btn-primary" @click="selectedComponent = 'chelsea'">Chelsea</button>
               <button class="btn btn-success" @click="selectedComponent = 'dortmund'">Dortmund</button>
               <button class="btn btn-danger" @click="selectedComponent = 'barcelona'">Barcelona</button>
               <br/><hr>
              
               <!-- <dortmund>
                 <img src="./assets/dortmund.png"/>
                 <h3>BVB</h3>
               </dortmund>
               <chelsea>
                 <img src="./assets/chelsea.png"/>
                 <h3>Chelsea</h3>
               </chelsea>
               <barcelona>
                 <img src="./assets/barcelona.png"/>
                 <h3>Barcelona</h3>
               </barcelona>  -->
              

               <component :is="selectedComponent">
                 <h2 style="font-family:Impact"> I &hearts; &#x26BD;</h2>
               </component>
    
            </div>
        </div>
    </div>

  </div>
</template>

<script>
import Dortmund from './components/dortmund'
import Chelsea from './components/chelsea'
import Barcelona from './components/barcelona'

export default {
  components: {
    dortmund: Dortmund,
    chelsea: Chelsea,
    barcelona: Barcelona
  },
  data: function(){
    return{
     selectedComponent: 'dortmund'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}

img{
  height:170px;
  width:170px;
}
</style>
