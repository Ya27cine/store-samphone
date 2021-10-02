<template lang="">
    <div>
        <h1>{{ marque }}</h1>

        <div class="row mx-1">
            <div class="col-md-4 col-ms-6" v-for="screen in screens">
                    <div class="card-group" >
                        <div class="card">
                            <img class="card-img-top" src="../../assets/model.png" alt="Card image cap">
                            <div class="card-body">
                                <h5 class="card-title">{{screen.Libelle}}</h5>
                                <div class="row ml-2">
                                       <h4> Quantite <span class="badge badge-info"> {{screen.Prix}} piece </span></h4>
                                       <button class="btn btn-success ml-4">+</button>
                                        <button class="btn btn-danger ml-2">-</button>                                      
                                </div>
                                <h4 class="card-title">model: {{screen.Modele}}</h4>
                                <h4 class="card-title">Color: {{screen.Color}}</h4>


                                <h4> Prix <span class="badge badge-danger"> {{screen.Prix}}€ </span></h4>

                            </div>
                        </div>
                     </div>
            </div>
        </div>
        
    </div>
</template>
<script>
export default {
    props: ['marque'],
    data() {
        return {
            screens: null
        }
    },
    mounted() {
         fetch("http://localhost:3000/screen").then( r => r.json() )
         .then( data =>  this.screens = data )
         .catch(e => console.log(e))

    },

}
</script>
<style>
.card-img-top{
   width: 128px!important;
   height: 128px!important;
}
.card-title{
    color: blue;
}
</style>