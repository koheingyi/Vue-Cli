<template>

   <div>

           <li class="list-group-item"  @dblclick="edit()">
               <input type="text" v-if="toedit"  @keyup.enter="toadd()" class="form-control" v-model="text" >
               <span v-else>{{text}}</span>
           </li>

   </div>
</template>

<script>
    export default {
        name: "todolist",
        data() {
            return {
                text: "",
                toedit:true,
            }
        },
        methods: {
            toadd() {
                    return this.toedit=false
            },
            edit(){
                return this.toedit=true
            }
        },
    }
</script>

<style scoped>

</style>