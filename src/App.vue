<template>
  <div class="app">

      <div class="q-pa-md doc-container">
        <center><img class src="../public/img/sincroniza.png" alt=""></center>
      </div>
    <div class="btns">
      <WhatsApp />

      <q-fab
        class="contato"
        color="white"
        text-color="white"
        icon="img:https://image.flaticon.com/icons/png/512/25/25419.png"
        direction="left"
      >
        <q-fab-action
          color="primary"
          text-color="white"
          @click="onClick"
          icon="img:https://img.icons8.com/ios/452/facebook-f.png"
          target="_blank"
          href="https://www.facebook.com/sincroniza.informatica"
        />

        <q-fab-action
          color="pink"
          text-color="white"
          @click="onClick"
          icon="img:https://www.radiogramadonews.com.br/wp-content/uploads/2020/06/logo-instagram-png-sem-fundo16.png"
          target="_blank"
          href="https://www.instagram.com/sincroniza.informatica/?hl=pt-br"
        />
      </q-fab>
    </div>

    
  </div>
</template>

<script>
import WhatsApp from "./components/WhatsApp.vue";
export default {
  name: "LayoutDefault",

  components: {
    WhatsApp,
  },

  data() {
    return {
      leftDrawerOpen: false,
    };
  },
};
</script>

<style>
body {
  height: 100px;
  width: 100px;
  background-color: black;
}

.btns {
  position: fixed;
  bottom: 30px;
  right: 10px;
  z-index: 9999;
  height: 150px;
  text-indent: -9999px;
  border-radius: 10px;
}

.q-parallax__media {
  display: none;
}

.logo{
   max-width: 150px;
}
</style>
