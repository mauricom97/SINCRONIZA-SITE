<template>
  <div class="social-midia">

    <q-fab
      class="contato"
      color="grey-8"
      text-color="white"
      icon="share"
      direction="right"
    >
      <q-fab-action
        color="primary"
        text-color="white"
        @click="onClick"
        icon="facebook"
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
</template>

<script>
export default {};
</script>

<style>

</style>