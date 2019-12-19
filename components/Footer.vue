<template>
    <footer>
        <div class="container-footer">
        <div>
            <h1>Sobre o GETA</h1>
            <p id="sobre">O grupo é registro no CNPQ na grande área de Tecnologias Socias</p>
        </div>
        <div>
            <h1>Navegação</h1>
            <ul>
                <li>Sobre</li>
                <li>Projetos</li>
                <li>Equipe</li>
                <li>Prêmios</li>
                <li>Parcerias</li>
            </ul>
        </div>
        <div>
            <h1>Contato</h1>
            <p>Email: geta@gmail.com</p>
            <p>Celular: (91) 99999-9999</p>
            <p>Endereço: Av. Alcindo Cacela, 1523 - Umarizal, Belém - PA, 66040-020</p>
        </div>
           <div>
            <h1>Rede Socias</h1>
            <a href="https://www.facebook.com/getacesupa/" target="_blank"><img src="~/assets/facebook-logo-white.svg" alt="" srcset=""></a>
        </div>
        </div>
        <h3>Copyright ©2019 Todos os direitos reservados para GETA</h3>

    </footer>
</template>

<script>


export default {
    
}
</script>

<style scoped>

footer{
background: #26A69A;
    padding: 1em 8em;
}
.container-footer{
    flex-direction: row;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

div{
    flex: 1;
    display: flex;
    flex-direction: column;
    color: white;
    min-width: 200px;
}

div h1{
    font-size: 16pt;
}

div ul{
    list-style: none;
    margin: 0;
    padding: 0;
}

div p {
    margin: 0;
    margin-bottom: 5px;
}

img{
    width: 7%;
}

#sobre{
        width: 200px;
}

h3{
    margin-top: 4em;
    font-size: 10pt;
    color: white;
    text-align: center;
    font-weight: 300;
}

@media (max-width: 800px) {
  footer{
      padding: 1em;
  }
}

</style>