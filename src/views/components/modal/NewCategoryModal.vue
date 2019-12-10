<template>
  <transition v-if="status" name="modal" class="modal-container">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">
                  <i data-feather="radio" class="tx-primary tx-12"></i> New
                  Category
                </h5>
                <button
                  type="button"
                  class="close"
                  data-dismiss="modal"
                  aria-label="Close"
                  @click="showAddNewCategoryModal"
                >
                  <span aria-hidden="true">&times;</span>
                </button>
              </div>
              <div class="modal-body">
                <form action="">
                  <div class="form-group mg-b-10">
                    <label for="">Category Name</label>
                    <input
                      type="text"
                      class="form-control"
                      placeholder="Riken Keiki Safety"
                    />
                  </div>
                  <table class="table table-hover">
                    <thead class="table-head">
                      <tr>
                        <th>Select</th>
                        <th>Card</th>
                        <th>Company Name</th>                        
                        <th>Phone No</th>
                        <th>Tags</th>
                        
                      </tr>
                    </thead>
                    <tbody>
                      <tr>
                        <td>
                            <div class="custom-control custom-checkbox">
                                <input type="checkbox" class="custom-control-input" id="customCheck1" checked>
                                <label class="custom-control-label" for="customCheck1"></label>
                            </div>
                        </td>
                        <td>
                          <img
                            class="card-img img-responsive"
                            src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                          />
                        </td>
                        <td>
                          We Care Services
                        </td>
                        
                        <td>555-777-3434</td>
                        
                        <td>
                          <p>
                            <span class="badge badge-info">Laptop Service</span>
                          </p>
                          <p>
                            <span class="badge badge-info">Mobile Service</span>
                          </p>
                        </td>
                        
                        
                      </tr>
                      <tr>
                        <td>
                            <div class="custom-control custom-checkbox">
                                <input type="checkbox" class="custom-control-input" id="customCheck1" checked>
                                <label class="custom-control-label" for="customCheck1"></label>
                            </div>
                        </td>
                        <td>
                          <img
                            class="card-img img-responsive"
                            src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                          />
                        </td>
                        <td>
                          We Care Services
                        </td>
                        
                        <td>555-777-3434</td>
                        
                        <td>
                          <p>
                            <span class="badge badge-info">Laptop Service</span>
                          </p>
                          <p>
                            <span class="badge badge-info">Mobile Service</span>
                          </p>
                        </td>
                        
                        
                      </tr>
                      <tr>
                        <td>
                            <div class="custom-control custom-checkbox">
                                <input type="checkbox" class="custom-control-input" id="customCheck1" >
                                <label class="custom-control-label" for="customCheck1"></label>
                            </div>
                        </td>
                        <td>
                          <img
                            class="card-img img-responsive"
                            src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                          />
                        </td>
                        <td>
                          We Care Services
                        </td>
                        
                        <td>555-777-3434</td>
                        
                        <td>
                          <p>
                            <span class="badge badge-info">Laptop Service</span>
                          </p>
                          <p>
                            <span class="badge badge-info">Mobile Service</span>
                          </p>
                        </td>
                        
                        
                      </tr>
                      <tr>
                        <td>
                            <div class="custom-control custom-checkbox">
                                <input type="checkbox" class="custom-control-input" id="customCheck1" >
                                <label class="custom-control-label" for="customCheck1"></label>
                            </div>
                        </td>
                        <td>
                          <img
                            class="card-img img-responsive"
                            src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                          />
                        </td>
                        <td>
                          We Care Services
                        </td>
                        
                        <td>555-777-3434</td>
                        
                        <td>
                          <p>
                            <span class="badge badge-info">Laptop Service</span>
                          </p>
                          <p>
                            <span class="badge badge-info">Mobile Service</span>
                          </p>
                        </td>
                        
                        
                      </tr>
                      <tr>
                        <td>
                            <div class="custom-control custom-checkbox">
                                <input type="checkbox" class="custom-control-input" id="customCheck1" checked>
                                <label class="custom-control-label" for="customCheck1"></label>
                            </div>
                        </td>
                        <td>
                          <img
                            class="card-img img-responsive"
                            src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                          />
                        </td>
                        <td>
                          We Care Services
                        </td>
                        
                        <td>555-777-3434</td>
                        
                        <td>
                          <p>
                            <span class="badge badge-info">Laptop Service</span>
                          </p>
                          <p>
                            <span class="badge badge-info">Mobile Service</span>
                          </p>
                        </td>
                        
                        
                      </tr>
                      
                    </tbody>
                  </table>
                </form>
              </div>
              <div class="modal-footer">
                <button
                  type="button"
                  class="btn btn-secondary"
                  data-dismiss="modal"
                  @click="showAddNewCategoryModal"
                >
                  Cancel
                </button>
                <button type="button" class="btn btn-add">Add Category</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>
<script>
import store from "../../../store/index.js";
export default {
  name: "NewCategoryModal",
  props: ["status"],
  methods: {
    showAddNewCategoryModal() {
      store.commit("toggleNewCategoryModal");
    }
  }
};
</script>
<style scoped>
.modal-container {
  font-size: 14px;
}
input.form-control {
  font-size: 14px;
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
.modal-header {
  margin-top: 0;
  background-color: #f95473;
  color: white;
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
.modal-dialog {
  overflow-y: initial !important;
}
.modal-body {
  height: 250px;
  overflow-y: auto;
}
.btn-add {
  background-color: #f95473;
  color: white;
}
.btn-add:hover {
  color: white;
}
</style>
