<template>
  <section id="info">
    <div class="container-image">
      <img src="~/assets/fotogeta.jpg" v-bind:class="{introImage:animation}" />
    </div>
    <div class="container-info" v-bind:class="{intro:animation}">
      <h1>Sobre nós</h1>
      <p>
        Proporcionamos independência à pessoas com deficiência através do desenvolvimento de protótipos e produtos de tecnologia asssistiva
        <br />
        <br />Economicamente viáveis e com tecnologia de integração nacional por meio de parcerias com núcleos de pesquisa nacionais e internacionais em tecnologia assistiva, terapia ocupacional, fisioterapia, psicologia, engenharia e tecnologia da informação.
      </p>
      <button>Saiba mais</button>
      <br />
      <div class="container-icon">
        <div>
          <img src="~/assets/trophy.svg" alt srcset />
          <h2>Missão</h2>
        </div>
        <div>
          <img src="~/assets/targett.svg" alt srcset />
          <h2>Objetivo</h2>
        </div>
        <div>
          <img src="~/assets/value.svg" alt srcset />
          <h2>Valores</h2>
        </div>
      </div>
    </div>
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
    handleScroll() {
      if (scrollY > 200 && this.animation == false) {
        this.animation = true;
      }
    }
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  }
};
</script>

<style scoped>
#info {
  height: 90vh;
  background: linear-gradient(90deg, rgb(231, 230, 230) 40%, #fff 20%);
  display: flex;
  justify-content: center;
}

.container-image {
  flex: 1;
  display: flex;

  justify-content: flex-end;
  align-items: center;
}

.container-image img {
  width: 550px;
  height: 550px;
  background: red;
  margin-right: 100%;
}

.introImage {
  animation: introImage 1s ease-in-out forwards;
}

@keyframes introImage {
  0% {
    margin-right: 100%;
  }

  75% {
    margin-right: -5%;
  }

  100% {
    margin-right: 0%;
  }
}

.container-info {
  flex: 1;
  padding: 4em 2em;
  opacity: 0;
  /* display: flex;
  flex-direction: column;
  justify-content: center; */
}

.container-info h1 {
  font-size: 28pt;
  margin: 0;
  margin-bottom: 0.5em;
  letter-spacing: -1px;
}

.intro {
  animation: showText 1s ease-out forwards;
}

@keyframes showText {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

.container-info p {
  margin: 0;
  line-height: 1.4;
  font-size: 12pt;
  letter-spacing: 1px;
  color: #6b6969;
}

.container-info button {
  padding: 12px 40px;
  background: #26a69a;
  outline: none;
  border: none;
  border-radius: 5px;
  font-size: 12pt;
  color: white;
  margin-top: 2em;
  transition: background-color 300ms linear;
  cursor: pointer;
}

.container-info button:hover {
  background: #125a53;
}

.container-icon {
  display: flex;
  flex-direction: row;
  padding: 1;
  align-items: flex-end;
  justify-content: space-between;
  margin-top: 3em;
  flex-wrap: wrap;
}

.container-icon div {
  display: flex;
  flex-direction: column;
  padding: 1em 2em;
  margin: 1em 2em;
}

.container-icon div h2 {
  font-size: 14pt;
  font-weight: 100;
  color: #6b6969;
}

@media (max-width: 800px) {
  #info {
    height: 100%;
    background: rgb(247, 247, 247);
    overflow: hidden;
    flex-wrap: wrap;
  }

  .container-icon {
    justify-content: center;
  }
}
</style>