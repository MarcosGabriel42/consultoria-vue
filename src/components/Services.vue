<template>
  <section id="servicos" class="services">
    <div class="container">
      <h2>Nossos Serviços</h2>

      <div class="cards">
        <div class="card" v-for="service in services" :key="service.title">
          <i :class="service.icon"></i>
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Services",
  data() {
    return {
      services: [
        {
          icon: "fas fa-chart-line",
          title: "Consultoria Estratégica",
          description: "Analisamos sua empresa e criamos um plano de crescimento estruturado."
        },
        {
          icon: "fas fa-laptop-code",
          title: "Transformação Digital",
          description: "Implementamos tecnologia para automatizar e modernizar processos."
        },
        {
          icon: "fas fa-users",
          title: "Treinamento de Equipes",
          description: "Capacitamos sua equipe para melhorar produtividade e organização."
        },
        {
          icon: "fas fa-bullseye",
          title: "Planejamento de Metas",
          description: "Definimos metas claras e alcançáveis para o seu negócio evoluir."
        }
      ]
    }
  }
}
</script>

<style scoped>
.services {
  padding: 120px 20px;
  background: #ffffff;
  text-align: center;
}

.services h2 {
  font-size: 36px;
  margin-bottom: 60px;
  color: #2d6cdf;
}

.cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 25px;
}

.card {
  background: #f5f7fb;
  padding: 35px 25px;
  border-radius: 14px;
  transition: 0.35s;
  cursor: pointer;
}

.card i {
  font-size: 40px;
  color: #2d6cdf;
  margin-bottom: 20px;
}

.card h3 {
  margin-bottom: 10px;
}

.card p {
  color: #555;
  line-height: 1.5;
}

.card:hover {
  transform: translateY(-12px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.15);
}

/* TABLET */
@media (max-width: 1000px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* CELULAR */
@media (max-width: 600px) {

  .services {
    padding: 90px 20px;
  }

  .cards {
    grid-template-columns: 1fr;
    gap: 18px;
  }

  .card {
    padding: 28px 20px;
  }

  .card i {
    font-size: 34px;
  }

  .card h3 {
    font-size: 18px;
  }

  .card p {
    font-size: 14px;
  }
}

</style>
