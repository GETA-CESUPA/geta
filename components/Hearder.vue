<template>
  <div class="navigacao">
    <input type="checkbox" id="bt_menu" />
    <label for="bt_menu">&#9776;</label>

    <nav class="menu">
      <ul>

     
     
        <li>
          <a href="#">Objetivos</a>
        </li>
           <li>
          <a href="#">Projetos</a>
        </li>
          <li>
          <a href="#">Equipe</a>
        </li>
           <li>
          <a href="#">Prêmios</a>
        </li>
           <li>
          <a href="#">Parcerias</a>
        </li>
              <li>
          <a href="#">Contato</a>
        </li>
     
      </ul>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.menu {
  margin: 0;
  width: 100%;
  height: 70px;
  background: #598cff;
  font-family: "Arial";
}

.menu ul {
  margin: 0;
  padding-top: 1em;
      padding-left: 9em;
  list-style: none;
  position: relative;
}

.menu ul li {
      width: 110px;
    font-size: 18px;
  background: tomato;
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
  background-color: rgba(0, 0, 0, 0.5);
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
  .navigacao {
    position: absolute;
    width: 100%;
  }

  label[for="bt_menu"] {
    display: block;
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
    background-color: #000;
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