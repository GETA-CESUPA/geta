<template>
  <section id="team">
    <h1>Nossa equipe</h1>
    <h2>O time é formado por estudantes e professores de varias áreas para maior efetividades das nossas ações</h2>
    <div class="container-equipe">
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
      </div>
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
      </div>
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
      </div>
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
      </div>
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
      </div>
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
      </div>
      <div class="membro">
        <img src="~/assets/fotogeta.jpg" alt />
        <p>Nome do aluno</p>
        <p>Cargo</p>
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
  letter-spacing: 1px;
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
    width:auto;
    text-align: center;
  }

  .container-equipe {
    justify-content: center;
  }
}
</style>