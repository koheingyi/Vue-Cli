<template>
    <div>
        <li class="list-group-item">
            {{ListText}}
            <button class="btn btn-outline-primary" @click="toRun">Run</button>
        </li>

    </div>
</template>

<script>
    export default {
        name: "list",
        props:["ListText","currentIndex"],
        methods: {
            toRun() {
              return this.$emit("toParent",this.currentIndex)
            }
        },

    }
</script>

<style scoped>

</style>