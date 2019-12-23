<template>
  <div class="navigacao">
    <input type="checkbox" id="bt_menu" />
    <label for="bt_menu">&#9776;</label>

    <nav class="menu" v-bind:class="{fixo:animation}">
      <ul>
        <li>
          <nuxt-link href="" to="/" id="home">         <img src="~/assets/getalogot.png" alt /></nuxt-link>
        </li>

        <li>
          <a href="#info">Sobre</a>
        </li>
        <li>
          <a href="#projects">Projetos</a>
        </li>

        <li>
          <a href="#container-awards">Prêmios</a>
        </li>
        <li>
          <a href="#team">Equipe</a>
        </li>
        <li>
          <a href="#partnerships">Parcerias</a>
        </li>

        <li>
          <a href="#footer">Contato</a>
        </li>
      </ul>
    </nav>
  </div>
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
      if (scrollY > 5) {
        this.animation = true;
      } else {
        this.animation = false;
      }
    }
  },

  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  }
};
</script>

<style scoped>
.menu {
  margin: 0;
  width: 100%;
  height: 70px;
  background: #598cff;
  font-family: "Arial";
  border-bottom: 1px solid rgba(255, 255, 255, 0.288);
}

.fixo {
  position: fixed;
  z-index: 3;
}

#home{
  background: none;
    padding: 0;
}

.menu ul {
  margin: 0;
  padding-top: 1em;
  padding-left: 9em;
  list-style: none;
  position: relative;
}

.menu ul li img {
  width: 80%;
}

.menu ul li {
  width: 110px;
  font-size: 16px;
  float: left;
}

.menu a {
  background-color: #598cff;
  padding: 15px;
  display: block;
  text-decoration: none;
  text-align: center;
  color: #fff;
}

.menu a:hover {
  font-weight: bold;
}

.menu ul ul {
  position: absolute;
  visibility: hidden;
}

.menu ul li:hover ul {
  visibility: visible;
}

.menu ul ul li {
  float: none;
  border-bottom: solid 1px #ccc;
}

.menu ul ul li a {
  background-color: #069;
}

label[for="bt_menu"] {
  padding: 5px;
  background-color: rgba(1, 39, 255, 0.2);
  color: #fff;
  font-family: "Arial";
  text-align: center;
  font-size: 30px;
  cursor: pointer;
  width: 50px;
  height: 50px;
  display: none;
}

#bt_menu {
  display: none;
}

@media (max-width: 800px) {
  .menu ul li img {
    width: 80%;
    display: none;
  }

  .navigacao {
    position: absolute;
    width: 100%;
  }

  label[for="bt_menu"] {
    /* display: block; */
  }

  #bt_menu:checked ~ .menu {
    margin-left: 0;
  }

  .menu {
    margin-top: 5px;
    margin-left: -100%;
    transition: all 0.4s;
  }

  .menu ul {
    padding: 0;
  }
  
  .menu ul li {
    width: 100%;
    float: none;
  }

  .menu a {
    background-color: rgb(72, 9, 245);
  }

  .menu ul ul {
    position: static;
    overflow: hidden;
    max-height: 0;
    transition: all 0.8s;
  }
  .menu ul li:hover ul {
    height: auto;
    max-height: 200px;
  }
}
</style>