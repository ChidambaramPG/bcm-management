<template>
  <div class="row">
      <div class="col-md-6">
          <div class="form-group">
                  <h5>Change Password</h5>
              </div>
          <form>
              <div class="form-group">
                  <label for="username">Old Password</label>
                  <input type="text" id="username" class="form-control"/>
              </div>
              <div class="form-group">
                  <label for="username">New Password</label>
                  <input type="text" id="username" class="form-control"/>
              </div>
              <div class="form-group">
                  <label for="username">Confirm Password</label>
                  <input type="text" id="username" class="form-control"/>
              </div>
              <button type="submit" class="btn update-btn">Update</button>
          </form>
      </div>
      <div class="col-md-6"></div>
  </div>
</template>

<script>
export default {
name:'ProfileSettings'
}
</script>

<style scoped>
.row{
    margin-top:20px;
}
.update-btn{
    background-color: #f95473;
    border-color: #f95473;
    color:white;
}

</style>