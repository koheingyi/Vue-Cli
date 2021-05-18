<template>
    <div>
            <h4>{{title}}</h4>
        <h4 class="badge bg-primary rounded">{{badgeTitle}}</h4>



    </div>
</template>

<script>
    export default {
        name:"Title",
        props:{
            title:{
                type:String,
                required:true,
                default:"this is Vue"

            },
            badgeTitle:{
                type: Number,
                default: 7,
                validator(value) {
                   return  value>5
                }

            }
        }
    }
</script>

<style lang="scss" scoped>

</style>