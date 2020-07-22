<template>
  <!-- <div id="animacao" :style="{ height: alturaAnimacao + 'px' }"> -->
  <div id="animacao">
    <div class="contentFlex">
      <i id="icone" :class="[iconeAnimacao, corAnimacao]"></i>
      <div id="tituloAnimacao" :style="{ color: corTexto }">
        {{ textoAnimacao }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    alturaAnimacao: String,
    iconeAnimacao: String,
    corAnimacao: String,
    corTexto: String,
    textoAnimacao: String
  }
}
</script>

<style lang="scss" scoped>
#animacao {
  height: 100vh;
  display: none;
  background: #fff;
  position: absolute;
  top: -10px;
  left: 0;
  width: 100%;
  z-index: 5;
  .contentFlex {
    display: flex;
    align-items: center;
    flex-direction: column;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -75%);

    i#icone {
      display: flex;
      font-size: 0%;
      transition: all 0.4s cubic-bezier(0.96, 0.12, 1, 1);
      &.tile-blue {
        color: #0180ff;
      }
      &.tile-turquoise {
        //tile-amethyst
        color: #00c6a5;
      }
      /* ASSIM Q SUBIR PARA PRODUÇÃO, ALTERAR COR DO SPACEMAN NO PORTAL ADM E EXCLUIR A CLASSE A BAIXO */
      &.tile-amethyst {
        //tile-amethyst
        color: #00c6a5;
      }
      /* ASSIM Q SUBIR PARA PRODUÇÃO, ALTERAR COR DO SPACEMAN NO PORTAL ADM E EXCLUIR A CLASSE A CIMA */
      &.tile-yellow {
        color: #ffcc00;
      }
      &.tile-black {
        color: #000;
      }
      &.tile-wisteria {
        color: #be04ff;
      }
      &.tile-purple {
        color: #700f60;
      }
      &.tile-pumpkin {
        color: #ff6e01;
      }
      &.tile-green {
        color: #99c422;
      }
    }
    #tituloAnimacao {
      display: flex;
      padding-top: 20px;
      font-size: 32px;
      transition: all 0.4s ease-in;
      position: relative;
      top: 400px;
    }
  }
}
</style>
