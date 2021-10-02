<template >
    <div>
        <h2>Store LCD :: SAMPHONE </h2>
        <ul v-for="screen in screens">
            <li >{{screen.Libelle}} </li>
        </ul>
    </div>
</template>
<script>
export default {
    data() {
        return {
            screens: null
        }
    },
    mounted() {
         fetch("http://localhost:3000/screen").then( r => r.json() )
         .then( data =>  this.screens = data )
         .catch(e => console.log(e))

         console.log('======')

         console.log(this.screens)


    },
    
}
</script>
<style>
    
</style>