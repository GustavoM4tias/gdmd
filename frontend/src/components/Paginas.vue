<script setup>

// Dados com títulos, descrições detalhadas e links para SVGs relacionados ao tema.
const cards = [
  {
    title: 'Site Responsivo',
    description: 'Um site responsivo é essencial para a experiência do usuário moderno. Ele se adapta a diferentes dispositivos como smartphones, tablets e desktops, ajustando automaticamente seu layout, imagens e conteúdo. A responsividade garante que seu site ofereça a melhor usabilidade, independentemente da tela usada.',
    imgSrc: 'https://www.svgrepo.com/show/530452/mobile-app.svg', // SVG relacionado a design responsivo
  },
  {
    title: 'Otimização e SEO',
    description: 'SEO (Search Engine Optimization) é o conjunto de estratégias que visa melhorar o posicionamento do seu site nos mecanismos de busca, como o Google. Otimizar seu site envolve melhorar sua velocidade, acessibilidade e relevância, utilizando palavras-chave e técnicas que aumentam sua visibilidade nos resultados de busca.',
    imgSrc: 'https://www.svgrepo.com/show/530440/machine-vision.svg', // SVG relacionado a SEO e otimização
  },
  {
    title: 'Site Gerenciável',
    description: 'Ter um site gerenciável significa que você pode fazer atualizações e edições de conteúdo de forma autônoma, sem precisar de conhecimentos técnicos avançados. Com um painel de controle intuitivo, é possível alterar textos, imagens, produtos e informações diretamente pelo navegador.',
    imgSrc: 'https://www.svgrepo.com/show/530456/host-record.svg', // SVG relacionado a gestão de sites
  },
  {
    title: 'Cross-browser',
    description: 'Cross-browser refere-se à capacidade do seu site de funcionar corretamente em todos os navegadores populares, como Chrome, Firefox, Safari e Edge. Isso é fundamental para garantir que todos os usuários tenham a mesma experiência, independentemente do navegador que estejam utilizando.',
    imgSrc: 'https://www.svgrepo.com/show/530443/interface-control.svg', // SVG relacionado a cross-browser
  },
  {
    title: 'Exclusividade',
    description: 'Desenvolver um site exclusivo significa criar uma identidade única para sua marca. Do design ao desenvolvimento, cada aspecto do site é personalizado para refletir a identidade visual e os valores do seu negócio, garantindo que você se destaque da concorrência.',
    imgSrc: 'https://www.svgrepo.com/show/530437/safe-and-stable.svg', // SVG relacionado a design exclusivo
  },
  {
    title: 'User Interface (UI)',
    description: 'UI (User Interface) refere-se ao design visual e à organização dos elementos que os usuários interagem em um site ou aplicativo. Uma boa UI deve ser esteticamente agradável, fácil de usar e promover uma navegação intuitiva, com botões, menus e formulários bem posicionados.',
    imgSrc: 'https://www.svgrepo.com/show/530458/touch-click.svg', // SVG relacionado à interface de usuário (UI)
  },
  {
    title: 'User Experience (UX)',
    description: 'UX (User Experience) é sobre como os usuários percebem e interagem com seu site. Fatores como velocidade de carregamento, acessibilidade e facilidade de navegação contribuem para uma experiência positiva. O objetivo é garantir que o usuário atinja seus objetivos no site de maneira rápida e eficiente.',
    imgSrc: 'https://www.svgrepo.com/show/530455/cloud-acceleration.svg', // SVG relacionado à experiência do usuário (UX)
  },
  {
    title: 'Blog e Newsletter',
    description: 'Um blog é uma excelente ferramenta para gerar tráfego para seu site e engajar seu público. Publicar conteúdo relevante, como artigos, notícias e tutoriais, ajuda a posicionar sua marca como uma autoridade no setor e melhora sua visibilidade nos mecanismos de busca.',
    imgSrc: 'https://www.svgrepo.com/show/530453/mail-reception.svg', // SVG relacionado a blogs
  },
];
</script>

<template>
  <div id="caracteristicas" class="container-fluid">
    <!-- Renderizamos cada card com layout alternado -->
    <div v-for="(card, index) in cards" :key="index" class="card-section d-flex align-items-center" :class="{'reverse-layout': index % 2 !== 0}">
      <!-- Coluna de texto -->
      <div class="text-container col-12 col-md-6 d-flex flex-column justify-content-center px-5">
        <h2 class="card-title">{{ card.title }}</h2>
        <p class="card-description">{{ card.description }}</p>
      </div>

      <!-- Coluna de imagem com SVG -->
      <div class="image-container col-12 col-md-6">
        <img :src="card.imgSrc" class="img-fluid" alt="Imagem relacionada ao {{ card.title }}">
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Estilos principais */
.container-fluid {
    background-color: #eef2f7;
}

.card-section {
  height: 100vh;
  display: flex;
  align-items: center;
  padding: 20px;
  background-color: #ffffff;
  transition: background-color 0.3s ease-in-out;
}

.card-section:nth-child(even) {
  background-color: #eef2f7;
}

.text-container {
  padding: 20px;
}

.card-title {
  font-size: 2.5rem;
  font-weight: bold;
  color: #333333;
  margin-bottom: 15px;
}

.card-description {
  font-size: 1.2rem;
  color: #555555;
}

.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image-container img {
  width: 80%;
  max-height: 70vh;
  object-fit: contain;
  border-radius: 10px;
}

/* Layout invertido */
.reverse-layout {
  flex-direction: row-reverse;
}

/* Responsividade */
@media (max-width: 768px) {
  .card-section {
    flex-direction: column;
    height: auto;
  }

  .reverse-layout {
    flex-direction: column;
  }

  .image-container img {
    max-height: 40vh;
  }
}
</style>
