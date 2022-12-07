<template>
  <div class="container">
      <HeaderTop projectName="TOP 5 RICHEST PEOPLE IN THE WORLD" />
      <RichestPersons :persons="persons" />
  </div>
</template>

<script>

    import HeaderTop from './components/HeaderTop.vue'
    import RichestPersons from './components/RichestPersons.vue'

    export default {
      name: 'App',
      components: {    
      HeaderTop,
      RichestPersons
    },

    data(){
      return {
        persons: []
      }
    },

    methods: {
      async fetchPersons(){
          const res = await fetch('https://nodes.herokuapp.com/api')
          const data = await res.json()
          console.log( data )
          return data.persons
      }
    },
    async created(){
    this.persons = await this.fetchPersons()
  }
}

</script>

<style>

    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      body {
        font-family: 'Montserrat', sans-serif;
      }
      .container {
        max-width: 720px;
        margin: 30px auto;
        overflow: auto;
        min-height: 300px;
        border: 0.3em solid black;
        padding: 30px;
        border-radius: 5px;
        background-color:rgb(200, 248, 250);
      }

      div{
        margin-bottom: 0.5em;
      }

</style>
