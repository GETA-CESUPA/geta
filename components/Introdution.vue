<template>
  <section >
    <Hearder/>
    <div class="container">
    <div class="introducao">
      <h1>GETA - Grupo de Estudo em Tecnologia do CESUPA</h1>
      <p>Somos um grupo focado na produção em estudos cientificos e tecnologia para pessoas com algum tipo de necessidade especial</p>
      <button>Conheça mais</button>
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
.container {
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
}

.introducao h1 {
  text-align: left;
  margin: 0;
  font-size: 36pt;
  color: white;
  font-weight: bold;
}

.introducao p {
  font-size: 16pt;
  text-align: left;
  color: white;
}

.introducao button {
  margin-top: 10px;
  text-align: left;
  background: #66d1ff;
  outline: none;
  border: none;
  padding: 12px 40px;
  font-size: 18px;
  color: white;
  border-radius: 5px;
  float: left;
  transition: background-color 300ms linear;
  cursor: pointer;
}

.introducao button:hover {
  background: #26a69a;
}

.imagem-pcc {
  flex: 1;
  padding-right: 10em;
}

.imagem-pcc img{
  width: 600px;
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

