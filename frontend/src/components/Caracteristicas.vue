<script setup>
import { ref } from 'vue';

const cards = ref([
    {
        icon: "fa-solid fa-mobile-screen",
        title: "Site Responsivo",
        text: "Seu site preparado para dispositivos móveis."
    },
    {
        icon: "fa-solid fa-chart-column",
        title: "Otimização e SEO",
        text: "Otimização do seu site para ranquear melhor nas buscas."
    },
    {
        icon: "fa-solid fa-gears",
        title: "Site gerenciável",
        text: "Edite e altere o conteúdo do seu site através do painel."
    },
    {
        icon: "fa-regular fa-window-restore",
        title: "Cross-browser",
        text: "Seu site com funcionalidade em qualquer navegador."
    },
    {
        icon: "fa-regular fa-file-zipper",
        title: "Exclusividade",
        text: "Design, key visual e programação exclusivos."
    },
    {
        icon: "fa-solid fa-user-check",
        title: "User Interface",
        text: "Design de interface amigável e fácil de navegar."
    },
    {
        icon: "fa-solid fa-computer-mouse",
        title: "User Experience",
        text: "Técnicas e interações focados na experiência usuário."
    },
    {
        icon: "fa-regular fa-newspaper",
        title: "Blog e Newsletter",
        text: "Sistema de blog e notícias para sua empresa converter."
    }
]);
</script>

<template>
    <div id="caracteristicas" class="container-fluid">
        <div class="container">
            <div class="textos d-flex pb-3 pt-5">
                <div class="titulo col-12 text-center pb-3">
                    <h4 class="fw-bold me-5">Principais características de um projeto de desenvolvimento de site:</h4>
                </div>
                <div class="col-12">
                    <p class="sub-texto me-4"><strong class="sub-texto">Criação de sites profissionais</strong> exclusivos, adaptados para
                        uma gama de dispositivos e planejados
                        para sua empresa conquistar ótimos resultados.</p>
                </div>
            </div>

            <div class="row g-4 pb-5">
                <div v-for="card in cards" :key="card.title" class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i :class="card.icon" class="mb-1"></i>
                            <h6 class="card-title mt-2">{{ card.title }}</h6>
                            <p class="card-text">{{ card.text }}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container-fluid {
    background-color: rgb(220, 238, 255);
}

.container {
    max-width: 100%;
    color: black !important;
}

.textos {
    flex-wrap: wrap;
}

.card {
    max-width: 100%;
    border: none;
    flex-grow: 1;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: 0.3s;
}

.card:hover {
    transform: scale(1.015);
    box-shadow: 4px 8px 12px rgba(0, 0, 0, 0.1);
    transition: 0.3s;
}

.card i {
    font-size: 1.5rem;
    color: #007bff;
}

.card i:hover {
    color: #006adb;
}

.card-title {
  font-size: 1.1rem;
}

.card-text {
  font-size: 0.8rem;
}

.sub-texto {
    font-size: 1rem;
}

@media (max-width: 728px) {
    .textos {
        flex-direction: column;
    }

    .card {
        margin-bottom: 20px;
    }

    .card-title {
        font-size: 1rem;
    }

    .card-text {
        font-size: 0.7rem;
    }
}
</style>