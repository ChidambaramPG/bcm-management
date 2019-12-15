<template>
  <section class="container mx-auto">
    <form class="form-signin">
      <img
        class="mb-4"
        src="../../assets/img/id-card.png"
        alt=""
        width="120"
        height="120"
      />
      <h1 class="h3 mb-3 font-weight-normal">Business Card Management</h1>
      <label for="inputEmail" class="sr-only">Email address</label>
      <input
        type="email"
        id="inputEmail"
        class="form-control"
        placeholder="Email address"
        required=""
        autofocus=""
      />
      <label for="inputPassword" class="sr-only">Password</label>
      <input
        type="password"
        id="inputPassword"
        class="form-control"
        placeholder="Password"
        required=""
      />
      <div class="checkbox mb-3">
        <label>
          <input type="checkbox" value="remember-me" /> Remember me
        </label>
      </div>
      <button class="btn btn-custom btn-block" type="submit">
        Sign in
      </button>
      <p class="mt-5 mb-3 text-muted">© 2019-2020</p>
    </form>
  </section>
</template>

<script>
export default {
    name:'Login'
};
</script>

<style scoped>
.container{
    background-color: #f9f9f9;
    padding:30px;
    margin-top:30px;
}
.form-signin{
    width:30% ;
    margin: 0 auto; 
    text-align:center;
}
input{
    margin-top:10px;
}

.btn-custom{
  background-color:#f95473;
}
</style>
