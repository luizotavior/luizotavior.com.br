<template>
  <div id="luiz">
    <div class="person"/>
  </div>
</template>

<script>

export default {
  data() {
      return {
      }
  }
}
</script>

<style lang="scss" scoped>
  div#luiz{
    height: 550px;
    width: 500px;
    background-image: url("/luiz-fundo.svg");
    background-position: center; /* Center the image */
    background-repeat: no-repeat; /* Do not repeat the image */
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    div.person{
      height: 390px;
      width: 120px;
      background-image: url("/luiz.svg");
      background-position: center; /* Center the image */
      background-repeat: no-repeat; /* Do not repeat the image */
    }
  }
</style>
