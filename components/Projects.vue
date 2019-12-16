<template>
  <section id="projects">
    <h4>Nossos Projetos</h4>
    <p>O grupo foca em várias em iniciativas voltadas para Tecnologia Assistiva e Social</p>
    <div class="container-projets">
      <div v-bind:class="{showImage1:animation}">
        <h2>Aplicativos</h2>
      </div>
      <div v-bind:class="{showImage2:animation}">
        <h2>Sistemas Web</h2>
      </div>
      <div v-bind:class="{showImage3:animation}">
        <h2>Artigos</h2>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      animation: false,
      type: "app",
      projets: [
        {
          integrantes: "Luan Wesley, Amaury Magalhães e Bruno De Masi",
          Solicitante:
            "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)",
          Descrição:
            "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.",
          responsável: "Alessandra Natasha",
          tipo: "app"
        },
        {
          integrantes: "Luan Wesley, Amaury Magalhães e Bruno De Masi",
          Solicitante:
            "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)",
          Descrição:
            "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.",
          responsável: "Alessandra Natasha",
          tipo: "app"
        },
        {
          integrantes: "Luan Wesley, Amaury Magalhães e Bruno De Masi",
          Solicitante:
            "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)",
          Descrição:
            "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.",
          responsável: "Alessandra Natasha",
          tipo: "app"
        },
        {
          integrantes: "Luan Wesley, Amaury Magalhães e Bruno De Masi",
          Solicitante:
            "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)",
          Descrição:
            "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.",
          responsável: "Alessandra Natasha",
          tipo: "app"
        },
        {
          integrantes: "Luan Wesley, Amaury Magalhães e Bruno De Masiii",
          Solicitante:
            "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)",
          Descrição:
            "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.",
          responsável: "Alessandra Natasha",
          tipo: "app"
        }
      ]
    };
  },

  methods: {
    filterProjets() {
      return this.projets.filter(f => f.tipo == this.type).splice(0, 3);
    },

    getNumberController() {
      return (
        parseInt(this.projets.filter(f => f.tipo == this.type).length / 3) + 1
      );
    }
  },

  methods: {
    handleScroll() {
      if (scrollY > 800) {
        this.animation = true;
        console.log("projetos", this.animation);
      }
    }
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  }
};
</script>

<style scoped>
#projects {
  text-align: center;
  padding: 1em 10em 2em 10em;
  margin-top: 4em;
}

#projects h4 {
  font-weight: bolder;
  font-size: 32pt;
  letter-spacing: 1px;
  margin: 10px 2em 10px 2em;
}

#projects p {
  color: #5f5d5d;
  font-size: 15pt;
}

.container-projets {
  display: flex;
  flex-direction: row;
  margin-top: 4em;
  justify-content: space-between;
  flex-wrap: wrap;
}

.container-projets div {
  background-image: url("../assets/app.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 350px;
  height: 300px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
}

.showImage1 {
  animation: showImage 1s ease-in forwards;
}

.showImage2 {
  animation: showImage 1s ease-in forwards 200ms;
}

.showImage3 {
  animation: showImage 1s ease-in forwards 400ms;
}

@keyframes showImage {
  from {
    margin-top: 10px;
    opacity: 0;
  }

  to {
    margin-top: 0;
    opacity: 1;
  }
}

.container-projets div h2 {
  color: white;
  z-index: 2;
}

.container-projets div::before {
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

.container-projets div:hover::before {
  background: rgba(0, 0, 0, 0);
}

.container-projets div:hover::before > h2 {
  display: none;
}

.container-projets div:nth-child(1) {
  background-image: url("../assets/app.jpg");
}

.container-projets div:nth-child(2) {
  background-image: url("../assets/web.jpg");
}

.container-projets div:nth-child(3) {
  background-image: url("../assets/artigo.jpg");
}

@media (max-width: 800px) {
  #projects {
    padding: 0;
  }

  
#projects h4 {
  font-size: 24pt;
}

#projects p {
    font-size: 12pt;
    padding: 1em 2em
}

  .container-projets div{
    width: 100%;
  }
}
</style> 