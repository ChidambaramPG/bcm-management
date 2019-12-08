<template>
  <transition v-if="status" name="modal" class="modal-container">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">
                        <i data-feather="radio" class="tx-primary tx-12"></i> Delete Brochure
                    </h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close" @click="showDeleteBrochureModal">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <h5>Are you sure?</h5>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-dismiss="modal" @click="showDeleteBrochureModal">Cancel</button>
                    <button type="button" class="btn btn-add">Delete Brochure</button>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    
  </transition>
</template>
<script>
import store from '../../../store/index.js';
export default {
  name: "DeleteBrochureModal",
  props:['status'],
  methods:{
        showDeleteBrochureModal(){
            store.commit('toggleDeleteBrochureModal')
        }
    }
};
</script>
<style scoped>
.modal-container{
    font-size:14px;
}
input.form-control{
    font-size:14px;
}
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: table;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.modal-container {
  width: 500px;
  margin: 0px auto;
  /* padding: 20px 30px; */
  background-color: #fff;
  border-radius: 5px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
  font-family: Helvetica, Arial, sans-serif;
}

.modal-header h3 {
  margin-top: 0;
  color: white;

}
.modal-header{
  margin-top: 0;
  background-color: #f11e1e;
  color:white;
}

.modal-body {
  margin: 20px 0;
}

.modal-default-button {
  float: right;
}
.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
.modal-dialog{
    overflow-y: initial !important
}
.modal-body{
    height: 80px;
    overflow-y: auto;
}
.btn-add{
    background-color:#f11e1e;
    color:white;
}
.btn-add:hover{
    color:white;
}
</style>
