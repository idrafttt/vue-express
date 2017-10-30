<template>
  <div class="login">
    <h1>Login</h1>

    <div><input type="email" name="email" v-model="email" placeholder="email address"/></div>
    <div><input type="password" name="password" v-model="password" placeholder="password"/></div>
    <button @click="login">Login</button>

  </div>
</template>

<script>
// import AuthenticationService from '@/services/AuthenticationService'

export default {
  name: 'Login',
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    async login () {
      alert(`Welcome back ${this.email}`)
    //   await AuthenticationService.login({
    //     email: this.email,
    //     password: this.password
    //   })
    }
  },
  watch: {
    email (value) {
      console.log('email has changed', value)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
