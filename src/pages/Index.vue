<template>
  <q-page class=" bg-grey-9 flex flex-center">
    <q-card style="width: 500px" class="q-mx-md bg-grey-9 text-white rounded-borders shadow-15">
      <q-card-section>
        <div class="text-h6 text-center text-uppercase">Comenzar</div>
      </q-card-section>
      <q-card-section class="q-mx-md text-center">
         <q-input  v-model="text" label="Nombre de usuario"  stack-label color="dark"  class="bg-white q-mb-xl rounded-borders"/>
         <q-input  v-model="text" label="Contraseña" color="dark"  class="bg-white q-mb-xl rounded-borders"/>
         <q-btn  :color="isDesktop ? 'primary': 'secondary'" class="text-capitalize q-px-xl q-mb-md rounded-borders" :label="isDesktop ? 'Entrar Desk': 'Entrar Móvil'" />
         
         <div class="row justify-center">
          <q-icon name="warning" class="q-mr-lg"/>
          <div class="text-caption">Olvide mi contraseña</div>
         </div>
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      isDesktop: this.$q.platform.is.desktop,
      text: null,
    }
  },
  created() {
    console.log('desktop', )
    console.log('mobile', this.$q.platform.is.mobile)
  },
};
</script>
