<template>
  <div class="container w-25">
    <h2 class="py-5 text-center">Login</h2>
    <form @submit.prevent="login">
      <!-- Email input -->
      <div class="form-outline mb-4">
        <label class="form-label" for="form2Example1">Email address</label>
        <input type="email" id="form2Example1" class="form-control" v-model="data.email" placeholder="Email address" name="email" />
      </div>

      <!-- Password input -->
      <div class="form-outline mb-4">
        <label class="form-label" for="form2Example2">Password</label>
        <input type="password" id="form2Example2" class="form-control" v-model="data.password" placeholder="Password" name="password" />
      </div>

      <!-- 2 column grid layout for inline styling -->
      <div class="row mb-4">
        <div class="col d-flex justify-content-center">
          <!-- Checkbox -->
          <div class="form-check">
            <input
              class="form-check-input"
              type="checkbox"
              value=""
              id="form2Example31"
              checked
            />
            <label class="form-check-label" for="form2Example31">
              Remember me
            </label>
          </div>
        </div>

        <div class="col">
          <!-- Simple link -->
          <a href="#!">Forgot password?</a>
        </div>
      </div>

      <!-- Submit button -->
      <button type="submit" class="btn btn-primary btn-block mb-4">
        Sign in
      </button>

      <!-- Register buttons -->
      <div class="text-center">
        <p>Not a member? <a href="#!">Register</a></p>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-google"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-twitter"></i>
        </button>

        <button type="button" class="btn btn-link btn-floating mx-1">
          <i class="fab fa-github"></i>
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: {
        email: '',
        password: ''
      }
    }
  },
  methods: {
    async login() {
      this.$auth.loginWith('local', {
        data: this.data
      })
      .then((response) => console.log('success'))
      .catch((error) => console.log('failed'));
    }
  }
};
</script>

<style>
</style>