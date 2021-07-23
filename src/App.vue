<template>
<div class = "container">
  
  <SearchBar @choose-sort-type ="storeSortType" @search-value="storeSearchType"/>
  <Tasks @toggle-reminder="toggleReminder" @delete-task ="deleteTask" :tasks="tasks" :sortType = "sortType" :name="name"/>

</div>
</template>

<script>

import Tasks from './components/Tasks'
import SearchBar from './components/SearchBar.vue'


export default {
  name: 'App',
  components: {
    Tasks,
    SearchBar
  },
  data(){
    return{
      tasks:[],
      showAddTask: false,
      sortType:0,
      name:""
    }
  },
  methods:{

    storeSortType(type){

      this.sortType = type;
      console.log(type)
    },
    storeSearchType(type){

      this.name = type;
      console.log(type)

    }


  },
 
  emits:[ 'search-value']
  ,
  created(){

    this.tasks = [

    ]

  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
  background-color:rgb(242,245,249)
}

.btn {
  display: inline-block;
  background: #000;
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  width: 100%;
}


.flex-column{
  display:flex;
  flex-direction:column;
  
}
.item-mobile{


}
.item-desktop{
  display:none;
}
@media screen and (min-width:400px){

.container-flex {


}
  .item-desktop{
    display:flex;
    flex-direction:row;
    flex-wrap:wrap;

  }
  .item-mobile{
    display:none;
  }



}
</style>
