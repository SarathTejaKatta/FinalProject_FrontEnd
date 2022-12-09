<template>
    <div class="bookbox">     

        <div v-for="person in persons" :key="person.id" >
            <PersonDetails :person="person"/>
        </div>

    </div>  
</template>

<script>

    import PersonDetails from './PersonDetails.vue'

    export default{
        name: 'RichestPerons',
        components: {
            PersonDetails
        },
        props:{
            
            persons: Array
        }
    }

</script>

<style scoped>

    .bookbox{
        background-color:rgb(75, 193, 252);
        padding: 1em;
        color: gray;
    }

</style>