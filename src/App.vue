<template>
  <div class="app">
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

    <q-parallax>


      <template v-slot:content="scope">
        <div
          class="absolute column items-center"
          :style="{
            opacity: 0.45 + (1 - scope.percentScrolled) * 0.55,
            top: scope.percentScrolled * 40 + '%',
            left: 0,
            right: 0,
          }"
        >
          <img
            src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg"
            style="width: 150px; height: 150px"
          />
          <div class="text-h3 text-white text-center">Sincroniza</div>
          <div class="text-h6 text-grey-3 text-center">informática</div>
        </div>
      </template>
    </q-parallax>
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
  bottom: 50px;
  right: 50px;
  z-index: 9999;
  height: 150px;
  text-indent: -9999px;
  border-radius: 10px;
}

.q-parallax__media{
  display: none;
}
</style>
