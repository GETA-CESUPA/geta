<template>
  <section>
    <h4>Nossos Projetos</h4>
    <p>O grupo foca em várias em iniciativas voltadas para Tecnologia Assistiva e Social</p>
    <div class="container-projets">
      <nuxt-link to="projets">
        <div v-bind:class="{showImage1:animation}">
          <h2>Sistemas</h2>
        </div>
      </nuxt-link>
      <nuxt-link to="projets">
      <div v-bind:class="{showImage2:animation}">
        <h2>Embarcados</h2>
      </div>
      </nuxt-link>
      <nuxt-link to="projets">
      <div v-bind:class="{showImage3:animation}">
        <h2>Artigos</h2>
      </div>
      </nuxt-link>
    </div>
    <nuxt-link to="projets">
    <p>Ver todos os projetos</p>
    </nuxt-link>
  </section>
</template>

<script>
export default {
  data() {
    return {
      animation: false
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
      if (scrollY > 700) {
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
  letter-spacing: -1px;
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
    opacity: 0;
  }

  to {
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

.container-projets a:nth-child(1) div {
  background-image: url("../assets/app.jpg");
}

.container-projets a:nth-child(2) div {
  background-image: url("../assets/embarcado.jpg");
}

.container-projets a:nth-child(3) div {
  background-image: url("../assets/artigo.jpg");
}

a {
  text-decoration: none;
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
    padding: 1em 2em;
  }

  .container-projets div {
    width: 100%;
  }

  a {
    width: 100%;
    text-decoration: none;
  }
}
</style> 