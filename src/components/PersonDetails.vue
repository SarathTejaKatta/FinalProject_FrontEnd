<template>

    <div>   
        <h2>{{person.name}}</h2>
        <h4>Father's Name: {{person.fathername}}</h4>
        <h4>Mother's Name: {{person.mothername}}</h4>
        <h4>Gender: {{person.gender}}</h4>
        <h4>Age: {{person.age}}</h4>
        <h4>DOB: {{person.dob}}</h4>
        <h4>Country: {{person.country}}</h4>
        <h4>NetWorth: {{person.networth}}</h4>

    </div>

</template>

<script>
    export default{
        name: 'PersonDetails',
        props:{
            person: Array
        }
    }
</script>

<style scoped>
    h4{
        margin: 2px;
    }

    div{
        background-color:rgb(149, 255, 160);
        color: black;
        padding: 1em;
    }
    .red{
        background-color: rgb(255, 72, 6) !important;
    }
    .green{
        color: white;
    }

</style>