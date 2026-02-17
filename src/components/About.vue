<template>
  <section id="sobre" class="about">
    <div class="container">
      <div class="about-text">
        <h2>Sobre a NovaEra</h2>
        <p>
          Somos uma empresa de consultoria focada em ajudar negócios
          a crescerem com organização, tecnologia e estratégia.
          Trabalhamos lado a lado com nossos clientes para encontrar
          soluções simples e eficientes.
        </p>
        <p>
          Nosso objetivo é modernizar processos, melhorar resultados
          e preparar sua empresa para o futuro digital.
        </p>
      </div>
      <div class="about-card">
        <h3>+{{ companies }}</h3>
        <span>Empresas atendidas</span>
        <h3>{{ years }}</h3>
        <span>de experiência</span>
        <h3>{{ satisfaction }}%</h3>
        <span>clientes satisfeitos</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",

  data() {
    return {
      companies: 0,
      years: 0,
      satisfaction: 0,
      animated: false
    }
  },

  mounted() {
    const observer = new IntersectionObserver((entries) => {
      if (entries[0].isIntersecting && !this.animated) {
        this.startCounters()
        this.animated = true
      }
    }, { threshold: 0.4 })

    observer.observe(this.$el)
  },

  methods: {

    animateValue(property, target, duration) {
      let start = 0
      const increment = target / (duration / 16)

      const timer = setInterval(() => {
        start += increment
        if (start >= target) {
          this[property] = target
          clearInterval(timer)
        } else {
          this[property] = Math.floor(start)
        }
      }, 16)
    },

    startCounters() {
      this.animateValue("companies", 120, 1500)
      this.animateValue("years", 8, 1500)
      this.animateValue("satisfaction", 95, 1500)
    }
  }
}
</script>


<style scoped>
.about {
  padding: 120px 20px;
  background: #f5f7fb;
}

.container {
  max-width: 1100px;
  margin: auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 50px;
  align-items: center;
}

.about-text h2 {
  font-size: 36px;
  margin-bottom: 20px;
  color: #2d6cdf;
}

.about-text p {
  line-height: 1.7;
  color: #444;
  margin-bottom: 15px;
}

.about-card {
  background: white;
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.08);
  text-align: center;
}

.about-card h3 {
  font-size: 32px;
  color: #2d6cdf;
  margin: 15px 0 5px;
}

.about-card span {
  display: block;
  color: #555;
  margin-bottom: 10px;
}

/* RESPONSIVO */
@media (max-width: 900px) {

  .container {
    grid-template-columns: 1fr;
    gap: 30px;
    text-align: center;
  }

  .about-text h2 {
    font-size: 28px;
  }

  .about-text p {
    font-size: 15px;
  }

  .about-card {
    padding: 30px 20px;
  }

  .about-card h3 {
    font-size: 26px;
  }
}

@media (max-width: 500px) {

  .about {
    padding: 90px 20px;
  }

  .about-text p {
    line-height: 1.6;
  }
}

</style>
