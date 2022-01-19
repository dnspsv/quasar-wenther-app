<template>
  <q-page class="flex flex-center bg-primary">
    <q-card class="">
      <img src="../assets/logo.png" ration="1" />

      <q-card-section class="q-pt-none">

        <q-input filled v-model="login.email" label="Email" />

        <q-input
          class="q-mt-sm"
          v-model="login.password"
          label="Password"
          filled
          :type="login.isPwd ? 'password' : 'text'"
        >
          <template v-slot:append>
            <q-icon
              :name="login.isPwd ? 'visibility_off' : 'visibility'"
              class="cursor-pointer"
              @click="login.isPwd = !login.isPwd"
            />
          </template>
        </q-input>

      </q-card-section>
      <q-card-actions class="full-width">
        <q-btn
          class="full-width q-mx-sm"
          color="primary"
          label="Login"
          style="wigth: 100%"
          @click="$router.push({ name: 'home' })"
        />
      </q-card-actions>
      <q-card-actions class="full-width">
        <q-btn
          flat
          no-caps
          class="full-width q-mx-sm"
          color="primary"
          label="Esqueci minha sanha"
          style="wigth: 100%"
          @click="$router.push({ name:'esqueciSenha'})"
        />
      </q-card-actions>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      login: {
        email: '',
        password: '',
        isPwd: true
      }
    }
  },
  methods: {}
}
</script>
