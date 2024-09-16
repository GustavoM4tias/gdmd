<template>
  <div class="metodologia">
    <h1 class="text-center mb-5">Nossa Metodologia</h1>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="metodologia-steps">
            <div class="step" v-for="(step, index) in steps" :key="index" :style="{ animationDelay: `${index * 500}ms` }">
              <div class="step-icon">
                <i :class="step.icon" class="fas fa-lg"></i>
              </div>
              <div class="step-content">
                <h2>{{ step.title }}</h2>
                <p>{{ step.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const steps = ref([
      {
        title: "Descoberta",
        description: "Entendemos suas necessidades",
        icon: "fa-lightbulb"
      },
      {
        title: "Planejamento",
        description: "Criamos um plano personalizado",
        icon: "fa-calendar-alt"
      },
      {
        title: "Design",
        description: "Criamos um design visual",
        icon: "fa-palette"
      },
      {
        title: "Desenvolvimento",
        description: "Construímos o site",
        icon: "fa-code"
      },
      {
        title: "Testes e Depuração",
        description: "Realizamos testes rigorosos",
        icon: "fa-bug"
      },
      {
        title: "Lançamento",
        description: "Lançamos o site",
        icon: "fa-rocket"
      },
      {
        title: "Manutenção e Suporte",
        description: "Oferecemos suporte contínuo",
        icon: "fa-wrench"
      }
    ]);

    return {
      steps
    };
  }
}
</script>

<style scoped>
.metodologia {
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.metodologia-steps {
  display: flex;
  flex-wrap: nowrap;
  justify-content: center;
}

.step {
  margin: 20px;
  width: calc(100% / 7);
  background-color: #f7f7f7;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  animation: slideInFromRight 2s ease-in-out;
}

.step-icon {
  text-align: center;
  margin-bottom: 10px;
}

.step-icon i {
  color: #007bff;
  font-size: 24px;
}

.step-content {
  text-align: center;
}

.step-content h2 {
  font-weight: bold;
  font-size: 18px;
  margin-bottom: 5px;
}

.step-content p {
  font-size: 14px;
  color: #666;
}

@keyframes slideInFromRight {
  0% {
    transform: translateX(100%);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}

/* Add media query for mobile devices */
@media only screen and (max-width: 768px) {
  .metodologia-steps {
    flex-wrap: wrap;
  }
  .step {
    width: 100%;
  }
}
</style>