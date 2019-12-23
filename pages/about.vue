<template>
    <section>
        <Hearder/>
        <div class="container-hearder">
<h1>Sobre</h1>
<hr>
<h2>Missão</h2>
<p>O Grupo de Estudos em Tecnologia Assistiva (GETA) exerce atividades de pesquisa e desenvolvimento no Centro Universitário do Estado do Pará (CESUPA) para pessoas com deficiência (paralisia cerebral, esclerose lateral amiotrófica, amiotrofia espinhal muscular infantil, ataxia, transtorno do espectro autista, deficiência visual, deficiência auditiva), deficiências físicas e/ou intelectuais. O GETA também organiza eventos e cursos de eletrônica e desenvolvimento de software para alunos e profissionais das áreas de Ciência e Engenharia da Computação, Sistemas de Informação e Engenharia Elétrica.</p>
<br>
<br>
<h2>Objetivos</h2>
<p>Proporcionar independência à pessoas com deficiência através do desenvolvimento de protótipos e produtos de tecnologia asssistiva economicamente viáveis e com tecnologia de integração nacional por meio de parcerias com núcleos de pesquisa nacionais e internacionais em tecnologia assistiva, terapia ocupacional, fisioterapia, psicologia, engenharia e tecnologia da informação.</p>
<br>
<br>
<h2>Valores</h2>
<p>Acreditar em Deus, acima de tudo; Respeitar as necessidades de pessoas com deficiência; Disponibilizar soluções de hardware e software com qualidade de mercado; Oferecer soluções economicamente viáveis e acessíveis.

</p>
        </div>
        <Footer/>
    </section>
</template>

<script>
import Hearder from "~/components/Hearder.vue";
import Footer from "~/components/Footer.vue";


export default {
 components: {
    Hearder,
    Footer
  }
}
</script>

<style scoped>
.container-hearder{
    padding: 1em 15em;
}

@media (max-width: 800px) {
    .container-hearder{
    padding: 1em 2em;
}
}
</style>

