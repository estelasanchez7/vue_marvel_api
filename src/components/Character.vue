<template>
    <div>
        <h3>Hello this is character.vue</h3>
        <p>{{this.$route.params.id}}</p>
    </div>
</template>

<script>
export default {
    name:'Character',
    props:{},
    setup(){
        return{

        }
    }
}
</script>

<style lang="scss">

</style>