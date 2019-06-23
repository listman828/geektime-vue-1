<template>
    <li @click="handleClick">{{content}}</li>
</template>

<script>
export default {
    props:['content','index'], //定义父组件传过来的属性，必须定义,有多个则定义多个参数 
    methods:{
        handleClick(){
            this.$emit("delete",this.index)
        }
    }
}
</script>

<style scope>

</style>
