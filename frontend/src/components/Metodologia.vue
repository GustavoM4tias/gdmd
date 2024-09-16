<script setup>
import { ref } from 'vue';

const methods = ref([
    {
        number: "01",
        title: "Briefing",
        description: "Imersão ao negócio<br>Benchmarking<br>Briefing<br>Definição de objetivos<br>Estudo de possibilidades",
        icon: "fas fa-briefcase"
    },
    {
        number: "02",
        title: "Arquitetura",
        description: "Sitemap<br>Mídias e tipos de conteúdo<br>Funcionalidade das páginas<br>Estruturação de conteúdo<br>Definição de materiais",
        icon: "fas fa-project-diagram"
    },
    {
        number: "03",
        title: "Design",
        description: "Wireframe<br>Keyvisual<br>User Interface<br>Protótipo<br>Layout",
        icon: "fas fa-paint-brush"
    },
    {
        number: "04",
        title: "Front-End",
        description: "Programação e codificação<br>Estruturação de páginas<br>Funcionalidades<br>Responsividade<br>CMS WordPress",
        icon: "fas fa-code"
    },
    {
        number: "05",
        title: "Homologação",
        description: "Revisão e testes<br>Integrações<br>Otimização SEO<br>Validação de conteúdo<br>Testes de performance",
        icon: "fas fa-check-circle"
    },
    {
        number: "06",
        title: "Entrega",
        description: "Entrega do projeto<br>Treinamento<br>Suporte inicial<br>Feedback<br>Documentação",
        icon: "fas fa-truck"
    }
]);
</script>

<template>
    <div class="container-fluid">
        <div class="container text-center py-5">
            <div class="row">
                <div class="col-12 pb-4">
                    <h1 class="titulo">Metodologia</h1>
                    <p class="subtitulo">Veja o que engloba nossa metodologia e entenda como funciona o nosso
                        processo de <span class="highlight">desenvolvimento de sites</span>.</p>
                    <a class="highlight orcamento text-decoration-none">Faça um orçamento</a>
                </div>
            </div>
            <div class="row">
                <div class="col-12 passos">
                    <div v-for="metodo in methods" :key="metodo.title" class="step">
                        <div class="passos-icone">
                            <i :class="metodo.icon" class="fa-lg" style="color: #4682b4;"></i>
                        </div>
                        <p class="passos-numero">{{ metodo.number }}</p>
                        <h2 class="passos-titulo">{{ metodo.title }}</h2>
                        <p class="passos-descricao" v-html="metodo.description"></p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container-fluid {
    background-color: #0a0f1e;
    color: #4682b4;
}

.titulo {
    font-size: 2.5rem;
    font-weight: bold;
}

.subtitulo {
    font-size: 1rem;
    color: #b0b0b0;
}

.highlight {
    color: #4682b4;
}

.step {
    text-align: center;
    margin-top: 2rem;
    position: relative;
    flex: 1;
}

.passos-icone {
    background-color: #1a1f2e;
    border-radius: 50%;
    padding: 0.5rem;
    margin-bottom: 1rem;
    width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
}

.passos-numero {
    font-size: 1rem;
    color: #b0b0b0;
}

.passos-titulo {
    font-size: 1.2rem;
    font-weight: bold;
}

.passos-descricao {
    font-size: 0.9rem;
    color: #b0b0b0;
}

.passos {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    flex-wrap: wrap;
}

.orcamento:hover {
    cursor: pointer;
    color: #50a3e7;
}

@media (max-width: 768px) {
    .step {
        flex: 0 0 48%;
        margin-bottom: 2rem;
    }
}
</style>