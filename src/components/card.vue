<template>
  <div>
    <h1>Card API</h1>
    <div style="display: flex;
    flex-wrap: wrap;
    justify-content: center;">
<div v-for = "item in storedata" style="margin-right: 10px;">
    <b-card no-body>{{item.id}}
        <b-card-group deck>
           <b-card img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top style="max-width: 240px;" class="mb-2">
             <b-card-title style="display: inline;">{{item.title}}</b-card-title>
          </b-card>
        </b-card-group>
    </b-card>
  
</div>
  </div>
</div>
</template>

<script>
import Vue from 'vue';
import VueAxios from 'vue-axios';
import axios from 'axios';
import Datacard from '../store';
Vue.use(VueAxios, axios)
export default{
  name: "card",
  data(){
    return{
      storedata: Datacard.data
    }
  },
  mounted(){
    Vue.axios.get('https://jsonplaceholder.typicode.com/todos/').then(resp=>{
      console.log(resp.data);
      this.storedata = resp.data;
    })
    .catch(function(error){
      console.log("Error", error);
    })
  }
}
  </script>