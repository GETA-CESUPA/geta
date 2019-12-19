<template>
  <section>
    <h1>Parcerias</h1>
    <h2>Unimos esforços com outras unidades para chegarmos no nosso proposito.</h2>
    <div class="container-parceiros">
      <a href="https://www.cesupa.br/" target="_blank">
        <img src="~/assets/cesupa.jpg" alt srcset />
      </a>
      <a href="http://www.nedeta.com.br/" target="_blank">
        <img src="~/assets/nedeta.jpg" alt srcset />
      </a>
      <a href="http://www.linkcomportamental.com/" target="_blank">
        <img src="~/assets/link.jpg" alt srcset />
      </a>
      <a href="http://www.aprende.ufpa.br/" target="_blank">
        <img src="~/assets/aprende.jpg" alt srcset />
      </a>
      <a href="http://web.mit.edu/" target="_blank">
        <img src="~/assets/mit.jpg" alt srcset />
      </a>
      <a href="https://www.cti.gov.br/pt-br" target="_blank">
        <img src="~/assets/cti.jpg" alt srcset />
      </a>
      <a href="http://www.finep.gov.br/" target="_blank">
        <img src="~/assets/finep.jpg" alt srcset />
      </a>
      <a href="http://www.fapespa.pa.gov.br/" target="_blank">
        <img src="~/assets/fapespa.jpg" alt srcset />
      </a>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
#partnerships {
  background: rgb(231, 230, 230);
  padding: 2em 10em;
}

h1 {
  text-align: center;
  font-weight: bolder;
  font-size: 32pt;
  letter-spacing: -1px;
  margin: 0;
}

h2 {
  text-align: center;
  font-size: 14pt;
  font-weight: 500;
  color: gray;
}
.container-parceiros {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}

.container-parceiros img {
  width: 220px;
  margin: 1em;
  filter: opacity(30%);
  transition: 300ms filter linear;
}

.container-parceiros img:hover {
  filter: opacity(100%);
}

@media (max-width: 800px) {
  #partnerships {
    padding: 1em 0em;
  }

  h2 {
    margin: 1em 2em;
  }

  .container-parceiros {
    justify-content: center;
  }
}
</style>