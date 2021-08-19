<template>
  <div class="wrapper">
    <div class="layout">
      <div class="background">
        <div class="colored-background"></div>
        <div class="line line--first"></div>
        <div class="line line--second"></div>
        <div class="line line--third"></div>
        <div class="line line--fourth"></div>
        <div class="line line--fifth"></div>
        <div class="first-left-stripe"></div>
        <div class="second-left-stripe"></div>
        <div class="left-stripe-blend"></div>
        <div class="right-stripe"></div>
      </div>
      <div class="content">
        <div class="content-layout">
          <div class="logo-container">
            <div class="logo">
              <stripe />
            </div>
          </div>
          <div class="form-container">
            <h1 class="card-title">Sign in to your account</h1>
            <form>
              <form-input title="Email" label-for="email" />
              <form-input title="Password" label-for="password" type="password">
                <template #link>
                  <nuxt-link to="">Forgot your password?</nuxt-link></template
                >
                <template #icon><eye-icon /></template>
              </form-input>
              <div class="input-container">
                <div class="checkbox-wrapper">
                  <input type="checkbox" />
                  <span>Stay signed in for a week</span>
                </div>
              </div>
              <div>
                <Button class="btn" @click="$router.push('/dashboard')">
                  Continue
                </Button>
                <div class="sso-link">
                  <nuxt-link to="">Use single sign-on (SSO) instead</nuxt-link>
                </div>
              </div>
            </form>
          </div>
          <footer-links />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import loginMeta from '~/data/loginMeta'
export default {
  data() {
    return {
      posts: [],
    }
  },
  fetch() {
    fetch('https://jsonplaceholder.typicode.com/posts')
      .then((response) => response.json())
      .then((json) => {
        this.posts = json
      })
    console.log(this)
  },
  head() {
    return {
      title: 'Login - Fidia',
      meta: loginMeta,
    }
  },
}
</script>
