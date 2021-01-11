<template>
  <div class="app">
    <center>
      <img
        class="laptop"
        src="https://www.flaticon.com/svg/vstatic/svg/689/689355.svg?token=exp=1610393669~hmac=ef6e7602cd2e85abc61a056b69423b0d"
        alt=""
      />
      <br />
      <div class="form q-gutter-md" style="max-width: 300px">
        <q-btn icon="email" id="contato" push color="primary" label="Contato">
          <q-popup-proxy>
            <q-card class="my-card">
              <q-card-section>
                <q-input borderless v-model="text" label="Seu nome" />
                <q-input borderless v-model="text" label="E-mail" />
                <q-input borderless v-model="text" label="Celular" />
                <q-input
                  v-model="text"
                  filled
                  type="textarea"
                  label="Descrição"
                />
                <br />
                <q-btn color="primary" label="Enviar" @click="informa_hora"/>

                <q-chat-message
                  v-if="status == 'success'"
                  class="mensagem"
                  name="Mauricio Nunes"
                  :stamp="hora"
                  :text="['Obrigado por seu contato, entraremos em contato em breve!']"
                  sent
                  text-color="white"
                  bg-color="primary"
                >
                  <template v-slot:avatar>
                    <img
                      class="q-message-avatar q-message-avatar--sent"
                      src="https://instagram.fbnu3-1.fna.fbcdn.net/v/t51.2885-19/s150x150/130947136_301344814571292_3483264615476889762_n.jpg?_nc_ht=instagram.fbnu3-1.fna.fbcdn.net&_nc_ohc=BtgjwMEkDAMAX9sq_cG&tp=1&oh=9f3cfa48b6872600408246908315b53d&oe=60245A9E"
                    />
                  </template>
                </q-chat-message>
              </q-card-section>
            </q-card>
          </q-popup-proxy>
        </q-btn>
      </div>
    </center>

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
      hora: null,
      status: null
    };
  },

  methods : {
    informa_hora(){
      this.hora = new Date().getHours() + ":" + new Date().getMinutes() + ":" + new Date().getSeconds()
      this.status = 'success';
    },
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
  position: absolute;
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

.laptop {
  max-width: 250px;
}

#contato {
  height: 80px;
  width: 150px;
}

.mensagem{
  max-width: 250px;
}
</style>
