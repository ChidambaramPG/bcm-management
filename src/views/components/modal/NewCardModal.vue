<template>
  <transition v-if="status" name="modal" class="modal-container">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">
                        <i data-feather="radio" class="tx-primary tx-12"></i> New Card
                    </h5>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close" @click="toggleNewCardModal">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body">
                    <form action="">
                        <div class="form-group mg-b-10">
                            <label for="">Name</label>
                            <input type="text" class="form-control" placeholder="Riken Keiki Safety">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Address</label>
                            <input type="text" class="form-control" placeholder="12B Baker Street">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Phone</label>
                            <input type="text" class="form-control" placeholder="555-444-3434">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Email</label>
                            <input type="email" class="form-control" placeholder="ikenkeiki@gmail.com">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Forecast</label>
                            <input type="text" class="form-control" placeholder="5M">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Requirements</label>
                            <input type="text" class="form-control" placeholder="Safety CDC">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Comments</label>
                            <input type="text" class="form-control" placeholder="Loem psum Dolor Sit Amet">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Contact</label>
                            <input type="text" class="form-control" placeholder="Abdul Rahman">
                        </div>
                        <div class="form-group mg-b-10">
                            <label for="">Business Card</label>
                            <input type="file" class="form-control" placeholder="Abdul Rahman">
                        </div>
                    </form>
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-dismiss="modal" @click="toggleNewCardModal">Cancel</button>
                    <button type="button" class="btn btn-add">Add Card</button>
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
  name: "NewCardModal",
  props:['status'],
  methods:{
        toggleNewCardModal(){
            store.commit('toggleNewCardModal')
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
  background-color: #f95473;
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
    height: 250px;
    overflow-y: auto;
}
.btn-add{
    background-color:#f95473;
    color:white;
}
.btn-add:hover{
    color:white;
}
</style>
