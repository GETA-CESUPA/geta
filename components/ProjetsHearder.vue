<template>
  <div>
    <Hearder />

    <section id="projets-hearder">
      <h1>Projetos Desenvolvidos</h1>
      <h2>Os projetos realizados objetivam a pesquisa e o desenvolvimento de produtos e soluções voltados para Tecnologia Social, como grande área e, mais especificamente, Tecnologia Assistiva, através de softwares e hardwares usáveis e economicamente acessíveis.</h2>
    </section>
    <section id="show-projets">
      <div class="container-select">
        <div
          v-for="t in tipos"
          :key="t"
          v-bind:class="{ selecionado: t == tipo}"
          @click="changeType(t)"
        >
          <h1>{{ t }}</h1>
        </div>
      </div>

      <div class="container-projets">
        <div class="projet-item" v-for="p in projetosCache" :key="p">
          <img :src="p.imagem" />
          <div>
            <h1>{{ p.nome }}</h1>
            <h2>{{ p.descricao }}</h2>
            <h2>Desenvolvedores: {{ p.integrantes }}</h2>
            <h2>Solicitante: {{ p.solicitante }}</h2>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Hearder from "~/components/Hearder.vue";

export default {
  components: {
    Hearder
  },

  data() {
    return {
      tipos: ["Todos", "Sistemas", "Embarcados", "Artigos"],
      tipo: "Todos",
      projetos: [
        {
          imagem: require("~/assets/getalogot.png"),
          nome: "Anatogame",
          integrantes: "Luan Wesley, Amaury Magalhães e Bruno De Masi",
          solicitante:
            "Fernanda Aguiar (Aluna PIBICT CESUPA - Curso de Medicina)",
          descricao:
            "Projeto que gamifica o estudo de anatomia para os cursos de ensino superior na área de saúde. Desenvolvimento de um aplicativo mobile/web.",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          imagem: "~/assets/getalogot.png",
          nome: "Ambiente Virtual de Aprendizagem",
          integrantes:
            "Amaury Magalhães, Luiz Ricardo, Otávio Araújo, Oscar Borges, Elielson Barbosa",
          solicitante: "Camylla Rocha(Aluna PIBICT CESUPA - Curso de Medicina)",
          descricao:
            "O projeto realiza simulação de procedimentos médicos para ensino de alunos de medicina em ambientes virtuais através da tecnologia de realidade virtual.",
          professor: "Alessandra Natasha",
          tipo: "Embarcados"
        },

        {
          imagem: "~/assets/getalogot.png",
          nome: "DTM - Disfunção Temporomandibular",
          integrantes: "Matheus Botelho, Renan Figueiredo",
          solicitante: "Katiane (Clínica de Fisioterapia do CESUPA)",
          descricao:
            "Projeto tem como finalidade de realizar o cálculo do desvio da disfunção temporomandibular, auxiliando o fisioterapeuta a saber em que estado se encontra",
          professor: "Alessandra Natasha",
          tipo: "Embarcados"
        },
        {
          nome: "Tracking de Marcha",
          integrantes:
            "Arthur Rocha, Eduardo Costa, Oscar Borges, David Cabral.",
          solicitante: "Wiviane Matos (Clínica de Fisioterapia do CESUPA)",
          descricao:
            "Criação de um sistema que auxilie na análise do movimento de marcha na fisioterapia, complementando o fisioterapeuta em seus exames.",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          nome: "Colete de Vibração",
          integrantes: "Paulo Amador, Larissa Negrão, Lucas Salame",
          solicitante: "Larissa Negrão (Clínica de Fisioterapia do CESUPA)",
          descricao:
            "Colete costurado com o intuito de ajudar na realização do processo de vibrocompressão, que consiste em mobilizar as secreções acumuladas nos pulmões do paciente, ajudando na respiração.",
          professor: "Alessandra Natasha",
          tipo: "Embarcados"
        },
        {
          nome: "Alzheimer VR",
          integrantes:
            "Larissa Negrão, Luiz Ricardo, Otávio Araújo, Oscar Borges, Pedro Lima, Luan Rodrigues.",
          solicitante: "Wiviane Matos (Clínica de Fisioterapia do CESUPA)",
          descricao:
            "Projeto que combina óculos de realidade virtual com aplicativo móvel, com o intuito de auxiliar no tratamento do mal de alzheimer.",
          professor: "Alessandra Natasha",
          tipo: "Embarcados"
        },

        {
          nome: "ECG",
          integrantes: "Matthews Gonçalves",
          solicitante: "Roberto Júnior (UFPa)",
          descricao:
            "Projeto que tem o intuito de criar um aparelho de eletrocardiograma de baixo custo para ajudar nos cursos de ensino superior na área de saúde. ",
          professor: "Alessandra Natasha",
          tipo: "Embarcados"
        },
        {
          nome: "Web-App de Apoio Oncológico",
          integrantes:
            "Bruno De Masi, Danilo Castro, Luiz Ricardo, Lucas Freitas, Victor Telles, Gabriel Cortez",
          solicitante: "Associação de Apoio Oncológico do Barros Barreto",
          descricao:
            "Criação de uma plataforma web para auxiliar na angariação de fundos para fornecer apoio a pessoas carentes que venham em busca de tratamento oncológico e não possuem recursos para se manterem na cidade, recrutamento de voluntariado para ações sociais.",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          imagem: require("~/assets/qd.jpg"),
          nome: "Quarto dimensão",
          integrantes: "Matheus Henrique dos Santos",
          solicitante: "Profa Dra Ana Irene (NEDETA/UEPa)",
          descricao:
            "Baseado em adaptações no ambiente residencial, agrega a mobilidade e promove a independência de pessoas com deficiência ou mobilidade reduzida, através da eletroencefalografia (EEG). O produto pode ser utilizado como um recurso de hardware adaptável a necessidade do usuário, a fim de promover a interface de controle residencial.",
          professor: "Alessandra Natasha",
          tipo: "Embarcados"
        },
        {
          imagem: require("~/assets/bl.jpg"),
          nome: "Brincando com a leitura",
          integrantes: "Matheus Henrique dos Santos.",
          solicitante:
            "Profa Dra Ana Irene (NEDETA/UEPa)Profa Dra Ana Irene (NEDETA/UEPa)",
          descricao:
            "Aplicativo desenvolvido para iOS e Android, que auxilia pessoas com deficiência física e/ou intelectual no processo da alfabetização, por meio do método fônico. A solução foi desenvolvida a partir de técnicas de gamificação e dotada de acessibilidade. Foi implementado um acionador baseado em bluetooth, que dispõe de tecnologia de integração nacional, economicamente acessível, através do qual o usuário pode se comunicar com o aplicativo por meio de tração, sopro, movimento da cabeça ou pressão.",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          imagem: require("~/assets/braille.jpg"),
          nome: "Brincando com Braille",
          integrantes: "Luís Fernando",
          solicitante: "Profa Alessandra Natasha",
          descricao:
            "Visa tornar a vida dos deficientes visuais mais fácil, através do reconhecimento de texto, é capaz de ler, textos nos mais variados ambientes através de um smartphone com câmera",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          imagem: require("~/assets/aprendendoOuvir.jpg"),
          nome: "Aprendendo a ouvir",
          integrantes: "Alder Furtado",
          solicitante: "Patrícia Madeira (Núcleo Aprende/UFPa)",
          descricao:
            "Aplicativo voltado para crianças com TEA (Transtorno do Espectro Autista) que visa induzir a interação social das mesmas por meio de estímulos auditivos em ambiente controlado",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          nome: "Site do Instituto Filippo Smaldone",
          integrantes: "Antonio Amaury Magalhães e Lucas Kzan",
          solicitante: "Irmã Círia(Instituto Filippo Smaldone)",
          descricao:
            "Site informativo, com finalidade de informar a história, descrição de atividades e ações  do Instituto",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          imagem: require("~/assets/vida+.png"),
          nome: "Vida+",
          integrantes: "Luan Wesley Siqueira Pereira",
          solicitante:
            "Patrícia Mendonça (Cesupa - Programa de Mestrado Profissional em Ensino em Saúde - Educação Médica)",
          descricao:
            "Aplicativo Android. É um guia médico do processo de transplantação de órgãos/tecidos, contendo informações de identificar doadores, quem notificar, quem encaminhar, etc",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          nome: "Braille Virtual",
          integrantes: "Luís Fernando",
          solicitante:
            "Centro de Referência em Inclusão Educacional Gabriel Lima Mender - CRIE",
          descricao:
            "aplicativo capaz de ensinar braile através de uma metodologia gamificada e inovadora",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"
        },
        {
          imagem: require("~/assets/peludinhos.jpg"),
          
          nome: "Peludinhos da UFPA",
          integrantes: "Alder Furtado, Victor Telles",
          solicitante: "Profa. Dra. Elizabeth  Pires (Peludinhos da UFPa)",
          descricao:
            "Trata-se de uma aplicação desenvolvida para auxiliar o procedimento de adoção de cães e gatos resgatados pela organização Peludinhos da UFPA. Neste website, é possível visualizar os pets resgatados e doar qualquer quantia para contribuir com as ações do projeto ou adotar os próprios pets",
          professor: "Alessandra Natasha",
          tipo: "Sistemas"

        }
      ],

      projetosCache: []
    };
  },

  mounted() {
    this.projetosCache = this.projetos;
  },

  methods: {
    changeType(tipo) {
      this.tipo = tipo;
      if (tipo == "Todos") {
        this.projetosCache = this.projetos;
      } else {
        this.projetosCache = this.projetos.filter(p => p.tipo == tipo);
      }
    }
  }
};
</script>

<style scoped>
#projets-hearder {
  width: 100%;
  height: 60vh;
  background: url("../assets/projets.jpg") no-repeat bottom;
  background-size: cover;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

#projets-hearder::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
}

#projets-hearder h1 {
  font-size: 32pt;
  text-align: center;
  color: white;
  z-index: 2;
}

#projets-hearder h2 {
  font-size: 13pt;
  color: white;
  z-index: 2;
  padding: 0em 12em;
  text-align: center;
  letter-spacing: 1px;
  font-weight: 300;
}

#show-projets {
  display: flex;
  flex-direction: column;
}

.container-select {
  margin-top: 3em;
  text-align: center;
  display: flex;
  justify-content: center;
}

.container-select div {
  width: 110px;
  border: 1.5px solid #26a69a;
  color: #26a69a;
  border-radius: 5px;
  padding: 2px 4px;
  cursor: pointer;
  transition: background-color 200ms linear;
}

.selecionado {
  background-color: #26a69a;
  color: white !important;
}

.container-select div h1 {
  margin: 0;
  font-size: 12pt;
  font-weight: 300;
}

.container-projets {
  padding: 0em 15%;
  display: flex;
  flex-direction: row;
  margin-top: 2em;
  flex-wrap: wrap;
  justify-content: center;
}

.projet-item {
  margin: 1em;
  width: 40%;
  border: 1px solid rgb(184, 184, 184);
  border-radius: 5px;
  display: flex;
  padding: 1em;
  transition: background-color 300ms linear;
}

.projet-item img {
  width: 60px !important;
  height: 60px !important;
  margin-right: 10px;
}

.projet-item h1 {
  margin: 0;
  font-size: 13pt;
  transition: color 300ms linear;
}

.projet-item h2 {
  font-size: 10pt;
  font-weight: 500;
  color: #525050;
  transition: color 300ms linear;
}

.projet-item p {
  font-size: 10pt;
  font-weight: bolder;
  float: right;
  margin: 0;
  cursor: pointer;
}

.projet-item:hover {
  background: #26a69a;
}

.projet-item:hover h1 {
  color: white;
}

.projet-item:hover h2 {
  font-size: 10pt;
  font-weight: 500;
  color: #fff0f0;
}

@media (max-width: 800px) {
  #projets-hearder {
    height: 80vh;
  }

  #projets-hearder h1 {
    font-size: 24pt;
  }

  #projets-hearder h2 {
    font-size: 10pt;
    padding: 0em 2em;
    line-height: 20px;
  }

  .container-projets {
    padding: 0em 5%;
  }

  .projet-item {
    width: 100%;
  }
}
</style>

