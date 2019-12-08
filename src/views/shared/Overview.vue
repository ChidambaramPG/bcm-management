<template>
    <div class="row">
        <div class="col-lg-3 col-md-6 overview-card">
            <div class="card">
                <div class="card-header">
                    Business Cards
                </div>
                <div class="card-body">                    
                    {{brochureCount}} <i class="fas fa-arrow-up fa-xs"></i>
                </div>
            </div>  
        </div>

        <div class="col-lg-3 col-md-6 overview-card">
            <div class="card">
                <div class="card-header">
                    Brochures
                </div>
                <div class="card-body">
                    {{businessCardCount}} <i class="fas fa-arrow-up fa-xs"></i>
                </div>
            </div>  
        </div>

        <div class="col-lg-3 col-md-6 overview-card">
            <div class="card">
                <div class="card-header">
                    Categories
                </div>
                <div class="card-body">
                    {{categoriesCount}} <i class="fas fa-arrow-up fa-xs"></i>                    
                </div>
            </div>  
        </div>

        <div class="col-lg-3 col-md-6 overview-card">
            <div class="card">
                <div class="card-header">
                    Users
                </div>
                <div class="card-body">
                    {{usersCount}} <i class="fas fa-arrow-down fa-xs"></i>
                    
                </div>
            </div>  
        </div>
      </div>
</template>

<script>
import store from '../../store/index.js';
export default {
    name:"Overview",
    computed:{
      brochureCount(){
        return store.state.brochureCount;
      },
      businessCardCount(){
        return store.state.businessCardsCount;
      },
      categoriesCount(){
        return store.state.categoriesCount;
      },
      usersCount(){
        return store.state.usersCount;
      },
      
      
    },
}
</script>

<style scoped>

.overview-card{
    padding:20px;
    height:80px;
    margin-top:20px;
}
.svg-inline--fa.fa-arrow-up{
    color:orange;
}
.svg-inline--fa.fa-arrow-down{
    color:red;
}

.card-header{
    background-color:#f95473;
    color: white;
    font-size:14px;
}

.card-body{
    font-size:14px;
    font-weight: 800;
    color:#212b5e;
}

</style>