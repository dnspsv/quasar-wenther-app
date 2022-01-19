<template>
  <q-page class="flex flex-center bg-primary">
    <q-card style="padding: 20px">

      <q-card-section class="q-pt-none full-width">
        <p class="text-h5">Esqueci minha senha</p>
        <div class="text-caption">Informe seu e-mail para recuperar a senha.</div>
      </q-card-section>

      <q-card-section class="q-pt-none full-width">
        <q-input filled v-model="email" label="Email" />
      </q-card-section>

      <q-card-actions class="full-width q-mt=sm">
        <q-btn
          class="full-width q-mx-sm"
          color="primary"
          label="Redefinir senha"
          style="wigth: 100%"
          @click="$router.push({ name: 'login' })"
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
      email: ''
    }
  },
  methods: {}
}
</script>
