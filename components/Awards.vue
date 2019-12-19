<template>
<section id="container-awards">
<h1>Prêmios</h1>
<h3>Durante nossa jornada, recebemos alguns prêmios sobre a causa</h3>
<div class="container-premios">
    <div>
        <img src="~/assets/3lugarXComputaçãoAmostra.jpg" alt="" srcset="">
        <h2>3º Lugar - X Computação Amostra</h2>
    </div>
    <div>
        <img src="~/assets/1lugarixCompamostra.jpg" alt="" srcset="">
        <h2>1º Lugar - IX Computação Amostra</h2>
    </div>
    <div>
        <img src="~/assets/conceicaoRangel.jpg" alt="" srcset="">
        <h2>Conceição Rangel - VIII Computação Amostra</h2>
    </div>
    <div>
        <img src="~/assets/premioexistir2016.jpg" alt="" srcset="">
        <h2>Prêmio EXISTIR 2016</h2>
    </div>

</div>
</section>
</template>

<script>

export default {

};
</script>

<style scoped>
#container-awards{
    background: #26A69A;
    padding: 1em 8em;
}

#container-awards h1{
    text-align: center;
      font-size: 30pt;
  color: white;
  font-weight: bold;
  margin-bottom: 0;
}

#container-awards h3{
      margin-bottom: 2em;
text-align: center;
    font-size: 14pt;
    font-weight: 200;
    color: #e2dfdf;
}

.container-premios{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
        justify-content: space-around;
}

.container-premios div{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.container-premios div img{
    width: 220px;
    border-radius: 100%;
}

.container-premios div h2{
    text-align: center;
    font-size: 14pt;
    color: white;
    font-weight: 300;
    width: 150px;
}

@media (max-width: 800px) {
  #container-awards{
       justify-content: center;
    padding: 1em 0em;
}

#container-awards h1{
      font-size: 24pt;

      margin-bottom: 1em;
}

.container-premios div{
    margin: 1em 0em
}

.container-premios div img{
    width: 220px;
}

}
</style>