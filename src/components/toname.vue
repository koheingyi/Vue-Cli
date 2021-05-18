<template>
    <div class="mt-5 w-25">
        <input type="text" class="form-control" v-model="text" @keyup.enter="add()">
        <ul class="list-group"  v-for="list in lists" :key="list" >
            <li class="list-group-item mt-3 ">
                {{list}}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name:"toname",
        data() {
            return {
                text:"",
                lists:[],
            }
        },
        methods: {
            add() {
                 this.lists.push(this.text)
                this.text=""
            }
        },
    }
</script>

<style scoped>

</style>