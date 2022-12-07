<template>
    <div>
        <h1> {{projectName}} </h1>
    </div>
</template>
    
<script>
    
    export default{
        name: 'HeaderTop',
        props:{
            projectName: String,
            projectDesc:String
        }
    }
    
</script>
    
<style scoped>
    
    div{
        text-align: center;
    }
    
</style>