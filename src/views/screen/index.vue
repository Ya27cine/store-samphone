<template >

    <div class="row" >
        <div class="col-md-4 col-ms-6">
            <div class="card" >
                <router-link  :to="{name: 'Show', params: {marque: 'samsung'}}">
                        <img class="card-img-top" src="../../assets/logo-SAMSUNG.png" alt="Card image cap">
                </router-link>
                <div class="card-body">
                  <p class="card-text">SAMSUNG</p>
                </div>
             </div> 
        </div>

        <div class="col-md-4 col-ms-6">
            <div class="card" >
                <router-link  :to="{name: 'Show', params: {marque: 'iphone'}}">
                        <img class="card-img-top" src="../../assets/logo-IPHONE.png" alt="Card image cap">
                </router-link>
                <div class="card-body">
                  <p class="card-text">IPHONE</p>
                </div>
             </div> 
        </div>


        <div class="col-md-4 col-ms-6">
            <div class="card" >
                <router-link  :to="{name: 'Show', params: {marque: 'huawei'}}">
                        <img class="card-img-top" src="../../assets/logo-HUAWEI.png" alt="Card image cap">
                </router-link>
                <div class="card-body">
                  <p class="card-text">HUAWEI</p>
                </div>
             </div> 
        </div>
    </div>
       
    
</template>
<script>
export default {
    
    
}
</script>
<style>
    
</style>