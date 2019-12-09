<template>
    <section id="projects">
        <h1>Nossos Projetos</h1>
        <div class="container-choice">
            <p>Aplicativos</p>
            <p>Sistemas Web</p>
            <p>Artigos</p>
        </div>
    </section>
</template>

<script>
export default {
    data(){
        return{
            projets: [
                {integrantes:"Luan Wesley, Amaury Magalhães e Bruno De Masi", Solicitante: "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)", Descrição: "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.", responsável: "Alessandra Natasha", tipo: "app"}
            ]
        }
    }
}
</script>

<style scoped>
#projects{
    text-align: center;
    padding: 1em 10em;
}

h1{
        font-weight: bolder;
    font-size: 32pt;
    letter-spacing: 1.2px;
}

.container-choice{
    display: flex;
    flex-direction: row;
    padding: 0em 10em;
    justify-content: space-around;
    align-items: center;
}

.container-choice p{
    font-size: 18pt;
    /* border-bottom: 3px solid grey; */
}
</style>