<script setup>
</script>

<template>
    <div class="container-fluid">

        <div class="container">
            <div class="textos d-flex py-5">
                <div class="titulo col-12 col-sm-6">
                    <h5 class="fw-bold me-5">Principais características de um projeto de desenvolvimento de site:</h5>
                </div>
                <div class="col-12 col-sm-6">
                    <p class="sub-texto me-4"><strong>Criação de sites profissionais</strong> exclusivos, adaptados para uma gama de dispositivos e planejados
                        para sua empresa conquistar ótimos resultados.</p>
                </div>

            </div>
            <div class="row g-4 pb-5">
                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-solid fa-mobile-screen mb-3"></i>
                            <h6 class="card-title mt-2">Site Responsivo</h6>
                            <p class="card-text">Seu site preparado para dispositivos móveis. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-solid fa-chart-column mb-3"></i>
                            <h6 class="card-title mt-2">Otimização e SEO</h6>
                            <p class="card-text">Otimização do seu site para ranquear melhor nas buscas. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-solid fa-gears mb-3"></i>
                            <h6 class="card-title mt-2">Site gerenciável</h6>
                            <p class="card-text">Edite e altere o conteúdo do seu site através do painel. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-regular fa-window-restore mb-3"></i>
                            <h6 class="card-title mt-2">Cross-browser</h6>
                            <p class="card-text">Seu site com funcionalidade em qualquer navegador. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-regular fa-file-zipper mb-3"></i>
                            <h6 class="card-title mt-2">Exclusividade</h6>
                            <p class="card-text">Design, key visual e programação exclusivos. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-solid fa-user-check mb-3"></i>
                            <h6 class="card-title mt-2">User Interface (UI)</h6>
                            <p class="card-text">Design de interface amigável e fácil de navegar. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-solid fa-computer-mouse mb-3"></i>
                            <h6 class="card-title mt-2">User Experience (UX)</h6>
                            <p class="card-text">Técnicas e interações focados na experiência usuário. </p>
                        </div>
                    </div>
                </div>

                <div class="col-6 col-sm-3">
                    <div class="card">
                        <div class="card-body">
                            <i class="fa-regular fa-newspaper mb-3"></i>
                            <h6 class="card-title mt-2">Blog</h6>
                            <p class="card-text">Sistema de blog e notícias para sua empresa converter. </p>
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
    color: black !important;
}

.sub-texto,
.sub-texto > strong {
    font-size: .8rem;
    color: rgb(85, 85, 85);
}

.card {
    border: none;
    height: 30vh;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: .3s;
}

.card:hover {
    transform: scale(1.015);
    box-shadow: 4px 8px 12px rgba(0, 0, 0, 0.1);
    transition: .3s;
}

.card i {
    font-size: 1.5rem;
    color: #007bff;
}

.card i:hover  {
    color: #006adb;
}

.card-text {
    font-size: .8rem;
}

@media (max-width: 728px) {
    .textos {
        flex-direction: column;
    }

    .sub-texto {
        margin-top: 10px;
    }


}
</style>
