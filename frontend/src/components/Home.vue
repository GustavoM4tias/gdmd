<script setup>
import { ref, onMounted } from 'vue';

const frases = [
    "Website",
    "Design",
    "Branding",
    "Digital",
];

const frase = ref(frases[0]);
const animEntrada = ref(true);
const animSaida = ref(false);

const alteraFrase = () => {
    let index = 0;
    setInterval(() => {
        animEntrada.value = false;
        animSaida.value = true;

        setTimeout(() => {
            index = (index + 1) % frases.length;
            frase.value = frases[index];
            animSaida.value = false;
            animEntrada.value = true;
        }, 1000);

    }, 3000);
};

onMounted(() => {
    alteraFrase();
});

function animacaoSaida(event) {
    if (event.animationName === 'saida') {
        animEntrada.value = false;
    }
}
</script>

<template>
    <div class="container-fluid vh-100">
        <div class="row h-100">

            <div class="col-12 col-md-6 d-flex justify-content-start align-items-center ps-5">
                <div class="text">
                    <p class="texto w-75">Soluções para seu negócio com:</p>
                    <p class="texto-animado fw-bold"
                        :class="{ 'animate-slide-in': animEntrada, 'animate-slide-out': animSaida }"
                        @animationend="animacaoSaida">
                        {{ frase }}
                    </p>
                </div>
                <a class="seta text-light position-absolute" href="#caracteristicas">
                    <i class="fa-solid fa-chevron-down fa-bounce" ></i>
                </a>
            </div>


            <div class="col-12 col-md-6 d-flex justify-content-center align-items-center position-relative">
                <div class="layer position-absolute z-0">
                    <img class="img pt-5" src="/layer.png" alt="">
                </div>
                <div class="phone position-absolute top-0 start-0">
                    <img class="position-absolute phone-2" src="/smartphone2.png" alt="">
                    <img class="position-absolute phone-1" src="/smartphone1.png" alt="">
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container-fluid {
    height: 100vh;
    color: azure !important;
    background-image: linear-gradient(to right top, #48138c, #331e81, #202374, #122565, #0d2455, #0b2854, #0d2c52, #123050, #113c5c, #0f4869, #0d5474, #0c617f);
}

@keyframes entrada {
    from {
        transform: translateY(-50px);
        opacity: 0;
    }

    to {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes saida {
    from {
        transform: translateY(0);
        opacity: 1;
    }

    to {
        transform: translateY(50px);
        opacity: 0;
    }
}

.texto-animado {
    font-size: 4rem;
    animation: entrada 1.05s ease-in, saida 1.05s ease-out 1.05s;
    animation-fill-mode: both;
    text-shadow: -15px 15px 40px rgba(11, 90, 194, .4), 15px -15px 40px rgba(108, 21, 221, .4);
}

.animate-slide-in {
    animation: entrada 1.05s ease-in forwards;
}

.animate-slide-out {
    animation: saida 1.05s ease-out;
}

.text {
    margin-left: 5rem;
}

.layer {
    overflow: hidden;
}

.img {
    height: 180vh;
}

.phone-1 {
    width: 30vw;
    margin-left: 1rem;
    margin-top: 6rem;
    filter: drop-shadow(-30px 30px 80px rgba(11, 90, 194, .4));
}

.phone-2 {
    width: 30vw;
    margin-left: 17vw;
    margin-top: 3em;
    transform: rotate(45deg);
    filter: drop-shadow(30px -30px 80px rgba(108, 21, 221, .4));
}

.phone-1 {
    animation: bounce 4s infinite;
}

.phone-2 {
    animation: bounce 5s infinite;
}

.seta {
    bottom: 10px;
    left: 25%;
}

.fa-bounce {
    animation-duration: 2s;
}


@keyframes bounce {

    0%,
    20%,
    50%,
    80%,
    100% {
        transform: translateY(0);
    }

    40% {
        transform: translateY(-20px);
    }

    60% {
        transform: translateY(-10px);
    }
}




@media (max-width: 728px) {

    .img {
        height: 180vw;
    }

    .text {
        margin-left: 0px;
    }

    .texto-animado {
        font-size: 3rem;
    }

    .phone-1 {
        width: 400px;
        margin-left: 15px;
        /* margin-top: 0px; */
        margin-top: -200px;
    }

    .phone-2 {
        /* 
        width: 450px;
        margin-left: 15px;
        margin-top: 500px; */
        display: none
    }

    .seta {
        bottom: 10px;
        left: 45%;
    }


}
</style>
