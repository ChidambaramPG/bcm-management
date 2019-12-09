<template>
  <div class="card-box">
    <div class="table-responsive">
      <div class="row table-row">
        <div class="col-md-12">
          <h5 class="table-title">
            <!-- <a href="/" class="sidebar-heading"> -->
              Categories
            <!-- </a> -->
          </h5>
          <div class="row">
            <div class="col-md-2">
              <ul class="list-group list-group-flush sidebar-list">
                <CategoriesSidebarMenu name="uncategorised" />
                <CategoriesSidebarMenu name="events" />
                <!-- <sidebar-menu-item name="brochures"/> -->
                <CategoriesSidebarMenu name="high profile" />
                <CategoriesSidebarMenu name="education" />
                <CategoriesSidebarMenu name="wedding" />
              </ul>
            </div>
            <div class="col-md-10">
              <table class="table table-hover">
                <thead class="table-head">
                  <tr>
                    <th>Card</th>
                    <th>Company Name</th>
                    <th>Address</th>
                    <th>Contact Person</th>
                    <th>Phone No</th>
                    <th>Added By</th>
                    <th>Action</th>
                    <th>Tags</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>
                      <img
                        class="card-img img-responsive"
                        src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                      />
                    </td>
                    <td>
                      We Care Services
                    </td>
                    <td>QBits Building, Vytilla Junction, Kerala</td>
                    <td>Rahul</td>
                    <td>555-777-3434</td>
                    <td>Administrator</td>
                    <td>
                      <a href="" @click.prevent="() => showEditCardsModal()"
                        ><i class="fas fa-edit text-success"></i
                      ></a>
                      <a href="" @click.prevent="() => showDeleteCardsModal()"
                        ><i class="fas fa-times text-danger"></i
                      ></a>
                    </td>
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
                      <img
                        class="card-img img-responsive"
                        src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                      />
                    </td>
                    <td>
                      We Care Services
                    </td>
                    <td>QBits Building, Vytilla Junction, Kerala</td>
                    <td>Rahul</td>
                    <td>555-777-3434</td>
                    <td>Administrator</td>
                    <td>
                      <a href="" @click.prevent="() => showEditCardsModal()"
                        ><i class="fas fa-edit text-success"></i
                      ></a>
                      <a href="" @click.prevent="() => showDeleteCardsModal()"
                        ><i class="fas fa-times text-danger"></i
                      ></a>
                    </td>
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
                      <img
                        class="card-img img-responsive"
                        src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                      />
                    </td>
                    <td>
                      We Care Services
                    </td>
                    <td>QBits Building, Vytilla Junction, Kerala</td>
                    <td>Rahul</td>
                    <td>555-777-3434</td>
                    <td>Administrator</td>
                    <td>
                      <a href="" @click.prevent="() => showEditCardsModal()"
                        ><i class="fas fa-edit text-success"></i
                      ></a>
                      <a href="" @click.prevent="() => showDeleteCardsModal()"
                        ><i class="fas fa-times text-danger"></i
                      ></a>
                    </td>
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
                      <img
                        class="card-img img-responsive"
                        src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                      />
                    </td>
                    <td>
                      We Care Services
                    </td>
                    <td>QBits Building, Vytilla Junction, Kerala</td>
                    <td>Rahul</td>
                    <td>555-777-3434</td>
                    <td>Administrator</td>
                    <td>
                      <a href="" @click.prevent="() => showEditCardsModal()"
                        ><i class="fas fa-edit text-success"></i
                      ></a>
                      <a href="" @click.prevent="() => showDeleteCardsModal()"
                        ><i class="fas fa-times text-danger"></i
                      ></a>
                    </td>
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
                      <img
                        class="card-img img-responsive"
                        src="https://www.digitalprinting.co.uk/media/images/products/slides/2/business-cards-1.jpg"
                      />
                    </td>
                    <td>
                      We Care Services
                    </td>
                    <td>QBits Building, Vytilla Junction, Kerala</td>
                    <td>Rahul</td>
                    <td>555-777-3434</td>
                    <td>Administrator</td>
                    <td>
                      <a href="" @click.prevent="() => showEditCardsModal()"
                        ><i class="fas fa-edit text-success"></i
                      ></a>
                      <a href="" @click.prevent="() => showDeleteCardsModal()"
                        ><i class="fas fa-times text-danger"></i
                      ></a>
                    </td>
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
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row pagination-row">
      <nav aria-label="Page navigation page-nav">
        <ul class="pagination justify-content-center">
          <li class="page-item">
            <a class="page-link" href="#" aria-label="Previous">
              <span aria-hidden="true">&laquo;</span>
              <span class="sr-only">Previous</span>
            </a>
          </li>
          <li class="page-item"><a class="page-link" href="#">1</a></li>
          <li class="page-item active"><a class="page-link" href="#">2</a></li>
          <li class="page-item"><a class="page-link" href="#">3</a></li>
          <li class="page-item">
            <a class="page-link" href="#" aria-label="Next">
              <span aria-hidden="true">&raquo;</span>
              <span class="sr-only">Next</span>
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>
<script>
import store from "../../../store/index.js";
import CategoriesSidebarMenu from "../categories/CategoriesSidebarMenu.vue";
export default {
  name: "CategoriesList",
  components: {
    CategoriesSidebarMenu
  },
  methods: {
    showEditCardsModal() {
      store.commit("toggleEditCardModal");
    },
    showDeleteCardsModal() {
      store.commit("toggleDeleteCardModal");
    }
  }
};
</script>
<style scoped>
a.sidebar-heading {
  display: block;
  /* height: 47px; */
  text-align: center;
  font-size: 25px;
  /* background-color: #212b5e; */
  color: #f95473;
  padding: 10px;
}

.sidebar {
  min-height: calc(100vh - 50px);
  font-size: 14px;
  transition: cubic-bezier(0.075, 0.82, 0.165, 1);
}

table {
  border-top: none;
  font-size: 14px;
}

th {
  font-weight: 400;
}
.table-title {
  padding: 10px;
}
.card-box {
  /* padding: 20px; */
  border: 2px solid #f3f3f3;
  -webkit-border-radius: 5px;
  border-radius: 5px;
  -moz-border-radius: 5px;
  background-clip: padding-box;
  /* margin-top: 100px; */
  margin-bottom: 20px;
  background-color: #ffffff;
}
.table-head {
  background-color: #f95473;
  color: white;
}
.pagination-row {
  padding-top: 10px;
}
nav {
  width: 100%;
}

li.page-item > a {
  color: #f95473;
  background-color: white;
}
li.page-item.active > a {
  color: #f95473;
  background-color: #212b5e;
  border-color: transparent;
}
.card-img {
  width: 50px;
  height: 50px;
}
</style>
