<template>
  <section >
    <Hearder/>
    <div class="container-introdution">
    <div class="introducao">
      <h1>GETA - Grupo de Estudo em Tecnologia do CESUPA</h1>
      <p>Somos um grupo focado na produção em estudos científicos e tecnologia para pessoas com algum tipo de deficiência</p>
      <nuxt-link to="about"> 
        <button>Conheça mais</button>
      </nuxt-link>
    </div>
    <div class="imagem-pcc">
      <img src="~/assets/galera.svg" alt="" srcset="">
    </div>
    </div>
    <Info/>
  </section>
</template>

<script>
import Hearder from "~/components/Hearder.vue";


export default {
  components: {
    Hearder,
  }
};
</script>

<style scoped>
.container-introdution {
  min-height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-wrap:wrap;
  background: #598cff;
}

.introducao {
  flex: 1;
  padding: 0em 0em 0em 10em;
  animation: showIntro 1s ease-in-out;
}

.introducao h1 {
  text-align: left;
  margin: 0;
  font-size: 36pt;
  color: white;
  font-weight: bold;
}

.introducao p {
  font-size: 14pt;
  text-align: left;
  color: white;
}

.introducao button {
  margin-top: 10px;
  text-align: left;
  background: #26A69A;
  outline: none;
  border: none;
  padding: 12px 40px;
  font-size: 17px;
  color: white;
  border-radius: 5px;
  float: left;
  transition: background-color 300ms linear;
  cursor: pointer;
}

.introducao button:hover {
  background: #125a53;
}

.imagem-pcc {
  flex: 1;
  padding-right: 10em;
}

.imagem-pcc img{
  width: 600px;
  opacity: 0;
  animation: showImg 1s linear 0.5s forwards;
}

@keyframes showImg {
  from{
    opacity: 0;
  }

  to{
    opacity: 1;
  }
}

@keyframes showIntro {
  from{
    opacity: 0;
    margin-top: 100px
  }

  to{
    opacity: 1;
    margin-top: 0px
  }
}

@media (max-width: 800px) {

  .introducao{
        padding: 1em 3em;
    padding-top: 6em;
    
  }

  .introducao h1{
    font-size: 20pt;
  }

  .introducao p {
    font-size: 12pt
  }

  .imagem-pcc{
    padding: 3em 0em;
  }

  .imagem-pcc img{
    width: 300px;
  }
}

@media (max-width: 320px) {

  .introducao button{
    padding: 10px 30px;
  }
}
</style>

