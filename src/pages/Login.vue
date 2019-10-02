<template>
  <transition
    appear
    enter-active-class="animated fadeIn"
    leave-active-class="animated fadeOut"
  >
    <q-layout view="hHh lpR fFf">
      <q-page-container>
        <q-page
          :style="loginPageStyle"
          class="absolute-full scroll"
          id="loginPage"
        >
          <div id="loginSpacer" style="height:10vh;" />
          <q-card class="q-ma-sm" dense id="loginCard" inline>
            <img :src="loginLogo" id="logo" style v-if="loginLogo" />
            <q-card-section>
              <q-form>
                <q-input
                  autocomplete="username"
                  autofocus
                  dark
                  label="Username"
                  name="username"
                  v-model="username"
                  v-on:keyup.enter="_login"
                ></q-input>
                <q-input
                  autocomplete="current-password"
                  dark
                  label="Password"
                  name="password"
                  type="password"
                  v-model="password"
                  v-on:keyup.enter="_login"
                ></q-input>
              </q-form>
            </q-card-section>
          </q-card>
        </q-page>
      </q-page-container>
    </q-layout>
  </transition>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      username: "",
      password: ""
    };
  },
  methods: { _login() {} }
};
</script>
