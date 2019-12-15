<template>
    <div class="row header-row">
        
        <div class="col-md-2" v-if="getCategorySection == 'table'">
            <button class="btn btn-block rounded btn-new" @click="setCategorySection">
                <i class="fas fa-plus-circle"></i><span> Add New</span>
            </button>
            
        </div>
        
    </div>

</template>
<script>
import store from '../../../store/index.js';
export default {
    name:'CategoriesHeader',
    methods:{
        showAddNewCategoryModal(){
            store.commit('toggleNewCategoryModal')
        },
        setCategorySection(){
            store.commit('setCategorySection','new');
        },
    },
    computed: {
        getCategorySection(){
            return store.state.categorySection;
        }
    },
}
</script>
<style scoped>
    .header-row{
        margin-top:10px;
    }
    .btn-new{
        background-color:#f95473;
        color:white;
    }
</style>