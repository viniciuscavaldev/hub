<script setup>

</script>

<template lang="pug">
div.background
  img(
    src="/images/logos.png"
  )
  p Desenvolvido por: Análise e planejamento - Caio Costa
</template>

<style scoped>
.background {
  background-image: url("/images/vetor.svg");
  height: 100vh;
  background-repeat: no-repeat;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  display: flex;
  flex-direction: column;
}
img {
  max-width: 80%;
}
p {
  justify-self: flex-end;
  opacity: 0.7;
}

@media screen and (max-height:680px) {
  .background {
  background-image: url("/images/vetor.svg");
  height: 100%;
  background-size: cover;
}
}
</style>
