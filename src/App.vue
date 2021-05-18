<template>
    <div class="p-4">
        <vuecli title="This is Vue CLi" :badge-title="8" ></vuecli>
       <ul>
         <List v-for="(fruit,index) in fruits" :list-text="fruit" :current-index="index" :key="index"  @toParent="del"></List>

       </ul>


        <ul class="list-group">
            <todolist></todolist>
        </ul>

        <toname></toname>



    </div>
</template>

<script>

import Vuecli from './components/vuecli.vue'
import List from "./components/list";
import Todolist from "./components/todolist";
import Toname from "./components/toname";




 export default {
  components: {Toname, Todolist, List,Vuecli},
     data() {
         return {
             fruits: ["apple","orange","Grape"],
         }
     },
     methods: {
         del(x) {
             return   this.fruits.splice(x,1)
         }
     },
       
    }
</script>

<style scoped>

</style>