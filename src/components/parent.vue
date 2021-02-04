<template>
<div>
        
        <label>Enter Job :</label>
        <input type="text" placeholder="Type your todos" v-model="t_name" size="30" rows="25">
        <button v-on:click="data_change()">+</button>
        <Child v-bind:jobs="jobs" v-on:deletejob="delete_job($event)" />
        <h1>Total number of jobs painding are {{jobs.length}}</h1>
 
</div>
</template>

<script>
import Child from './Child.vue'
export default {
 name:"parent",
 components:{
     Child,
 } ,
data(){
    return{
        jobs:[
            {name:"Wash Cloths",id:1},
            {name:"make lunch",id:2},
            {name:"study",id:3}

        ],
        t_name:" ",
        t_id:4
        
    }
},

methods:{
    
       data_change()
       {
           
       
         this.jobs.push({name:this.t_name,id: this.t_id++})
         
         },
       delete_job(id){
           
          this.jobs = this.jobs.filter(x => x.id != id);
         },
        
    }


};
</script>

<style scoped>
button {
    background-color: rgb(153, 128, 172);
   border: none;
  color: white;
  padding: 2px;
  text-align: center;
  text-decoration: none;
  
  font-size: 12px;
  margin: 4px;
  border-radius: 50px;
  float: right;
  margin-left: -50%;
   margin-top: 25px;
   padding: 6px;
   margin-right:20px;

  
}
h1{
     font-family: cursive;
     font-size:15px;
     color:rgb(161, 159, 159);
}
label{
    margin-top: 25px;
    padding: 10px;
}
input{
     margin-top: 25px;
}
input[type=text]:focus {
  border: 2px solid #555;
}


</style>