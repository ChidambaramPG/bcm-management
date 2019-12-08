<template>
    <div>
        <new-brochure-modal v-if="showNewBrochureModal" :status="showNewBrochureModal"/>
        <new-card-modal v-if="showNewCardModal" :status="showNewCardModal"/> 
        <edit-brochure-modal v-if="showEditBrochureModal" :status="showEditBrochureModal"/>
        <delete-brochure-modal v-if='showDeleteBrochureModal' :status='showDeleteBrochureModal' />
        <edit-card-modal v-if="showEditCardModal" :status='showEditCardModal' />
        <delete-card-modal v-if='showDeleteCardModal' :status='showDeleteCardModal' />
    </div>
</template>
<script>
import NewBrochureModal from '../components/modal/NewBrochureModal.vue';
import NewCardModal from '../components/modal/NewCardModal.vue';
import EditBrochureModal from '../components/modal/EditBrochureModal.vue';
import DeleteBrochureModal from '../components/modal/DeleteBrochureModal.vue';
import EditCardModal from '../components/modal/EditCardModal.vue';
import DeleteCardModal from '../components/modal/DeleteCardModal.vue';
import store from '../../store/index.js';
export default {
    name:'AllModals',
    components:{
        NewBrochureModal,
        NewCardModal,
        EditBrochureModal,
        DeleteBrochureModal,
        EditCardModal,
        DeleteCardModal
    },
    computed:{
        showNewBrochureModal(){
            return store.state.newBrochureModalVisible;
        },
        showNewCardModal(){
            return store.state.newCardsModalVisible;
        },
        showEditBrochureModal(){
            return store.state.editBrochureModalVisible;
        },
        showDeleteBrochureModal(){
            return store.state.deleteBrochureModalVisible;
        },
        showEditCardModal(){
            return store.state.editCardsModalVisible;
        },
        showDeleteCardModal(){
            return store.state.deleteCardsModalVisible;
        },
    }
}
</script>