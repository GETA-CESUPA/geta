<template>
  <section id="team">
    <h1>Nossa equipe</h1>
    <h2>O time é formado por estudantes, egressos e professores de várias áreas para maior efetividade das nossas ações</h2>
    <div class="container-equipe">
      <div class="membro">
        <img src="~/assets/alder.png" alt />
        <p>Alder Furtado</p>
        <p>Ciência da Computação</p>
      </div>
      <div class="membro">
        <img src="~/assets/alessandra.jpg" alt />
        <p>Alessandra Baganha</p>
        <p>Professora</p>
      </div>
      <div class="membro">
        <img src="~/assets/amauryjunior.png" alt />
        <p>Amaury Magalhães</p>
        <p>Eng. da Computação</p>
      </div>
      <div class="membro">
        <img src="~/assets/arnaldo.png" alt />
        <p>Arnaldo Prado</p>
        <p>Eng. de Produção</p>
      </div>
      <div class="membro">
        <img src="~/assets/arthurrocha.png" alt />
        <p>Arthur Rocha</p>
        <p>Ciência da Computação</p>
      </div>
      <div class="membro">
        <img src="~/assets/brunodemasi.png" alt />
        <p>Bruno De Masi</p>
        <p>Ciência da Computação</p>
      </div>
      <div class="membro">
        <img src="~/assets/caiobastos.png" alt />
        <p>Caio Basto</p>
        <p>Eng. da Computação</p>
      </div>
      <div class="membro">
        <img src="~/assets/eduardocosta.png" alt />
        <p>Eduardo Costa</p>
        <p>Ciência da Computação</p>
      </div> 
        <div class="membro">
        <img src="~/assets/fernando.jpg" alt />
        <p>Fernando Gomes</p>
        <p>Ciência da Computação</p>
      </div> 
        <div class="membro">
        <img src="~/assets/gabrielcortez.png" alt />
        <p>Gabriel Cortez</p>
        <p>Ciência da Computação</p>
      </div> 
        <div class="membro">
        <img src="~/assets/larissanegrao.png" alt />
        <p>Larissa Negrão</p>
        <p>Ciência da Computação /<br> Fisioterapia</p>
      </div> 
       <div class="membro">
        <img src="~/assets/LuanPereira.png" alt />
        <p>Luan Pereira</p>
        <p>Eng. da Computação</p>
      </div> 
        <div class="membro">
        <img src="~/assets/lucassalame.png" alt />
        <p>Lucas Salame</p>
        <p>Eng. da Computação</p>
      </div>
        <div class="membro">
        <img src="~/assets/matheusbotelho.png" alt />
        <p>Matheus Botelho</p>
        <p>Ciência da Computação</p>
      </div>
        <div class="membro">
        <img src="~/assets/matheus.jpg" alt />
        <p>Matheus Henrique</p>
        <p>Ciência da Computação</p>
      </div>
         <div class="membro">
        <img src="~/assets/raphael.jpg" alt />
        <p>Raphael Rocha</p>
        <p>Ciência da Computação</p>
      </div>
        <div class="membro">
        <img src="~/assets/victortelles.png" alt />
        <p>Victor Telles</p>
        <p>Ciência da Computação</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
#team {
  padding: 2em 10em;
}

h1 {
  font-weight: bolder;
  font-size: 32pt;
  letter-spacing: -1px;
  margin: 0;
}

h2 {
        width: 630px;
    font-size: 14pt; 
    font-weight: 500;
    color:gray;
    margin-bottom: 2em;
}

.container-equipe {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.membro {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

.membro img {
  width: 200px;
  border-radius: 100%;
  margin-bottom: 10px;
}

.membro img::before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
  background: rgba(0, 0, 0, 0.6);
  transition: background-color 500ms linear;
  cursor: pointer;
}


.membro p {
  margin: 3px;
}

@media (max-width: 800px) {
  #team {
    padding: 1em 0em;
  }

  h1 {
    font-size: 24pt;
    text-align: center;
  }

  h2 {
    font-size: 12pt;
    padding: 0em 2em;
    width:auto;
    text-align: center;
  }

  .container-equipe {
    justify-content: center;
  }
}
</style>