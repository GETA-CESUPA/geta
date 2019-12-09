<template>
  <section id="info">
    <div class="container-info">
      <img src="~/assets/trophy.svg" alt srcset />
      <h1>Missão</h1>
      <p>O Grupo de Estudos em Tecnologia Assistiva (GETA) exerce atividades de pesquisa e desenvolvimento no Centro Universitário do Estado do Pará (CESUPA) para pessoas com deficiência (paralisia cerebral, esclerose lateral amiotrófica, amiotrofia espinhal muscular infantil, ataxia, transtorno do espectro autista, deficiência visual, deficiência auditiva), deficiências físicas e/ou intelectuais. O GETA também organiza eventos e cursos de eletrônica e desenvolvimento de software para alunos e profissionais das áreas de Ciência e Engenharia da Computação, Sistemas de Informação e Engenharia Elétrica.</p>
    </div>
    <div class="container-info"> 
      <img src="~/assets/targett.svg" alt srcset />
      <h1>Objetivos</h1>
      <p>Proporcionar independência à pessoas com deficiência através do desenvolvimento de protótipos e produtos de tecnologia asssistiva economicamente viáveis e com tecnologia de integração nacional por meio de parcerias com núcleos de pesquisa nacionais e internacionais em tecnologia assistiva, terapia ocupacional, fisioterapia, psicologia, engenharia e tecnologia da informação.</p>
    </div>
    <div class="container-info">
      <img src="~/assets/value.svg" alt srcset />
      <h1>Valores</h1>
      <p>Acreditar em Deus, acima de tudo; Respeitar as necessidades de pessoas com deficiência; Disponibilizar soluções de hardware e software com qualidade de mercado; Oferecer soluções economicamente viáveis e acessíveis.</p>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style scoped>
#info {
  display: flex; 
  padding: 0em 10em;
  flex-wrap: wrap;
}

.container-image {
  flex: 1.5;
  background-color: #26A69A
}

.container-info{
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 3em 2em 1em 2em;

}

.container-info h1{
  font-weight: 100;
}

.container-info p{
      letter-spacing: 1.2px;
    word-spacing: 2px;
    line-height: 23px;

    height: 250px;
    overflow: auto;
    text-overflow: ellipsis;

}

@media (max-width: 800px) {
#info{
padding: 0em;
}

}

</style>