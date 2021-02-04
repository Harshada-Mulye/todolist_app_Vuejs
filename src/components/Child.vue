<template>
  <div>
    <ul>
    <li v-for="job in jobs" :key="job.id">
        {{job.name}}
        <button v-on:click="delete_job(job.id)">X</button>
       
    </li>
    </ul>
    <h4>{{name}}</h4>
  </div>
</template>

<script>
export default {
  name: "Child",
  props: ["jobs"],
   methods:{
       delete_job(id){
         // console.log("Hello")
        
      this.$emit('deletejob',id)
       }
    }
};
</script>

<style scoped>


ul{
  list-style: none;
   font-family: cursive;
  padding: 10px;
   text-align: left;
}
li:nth-child(odd) {
  background: rgb(211, 226, 170);
}
li:nth-child(even) {
  background: rgb(237, 237, 238);
}

button{
    
  border: none;
  color: white;
  padding: 2px;
  text-align: center;
  text-decoration: none;
  
  font-size: 16px;
  margin: 4px;
  border-radius: 2px;
  float: right;
  margin-left: -50%;
  
  
  
}
</style>
