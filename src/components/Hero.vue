<template>
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Transformando ideias em resultados</h1>
      <p>
        A NovaEra é uma consultoria especializada em ajudar empresas
        a crescerem com estratégia, tecnologia e inovação.
      </p>

      <a href="#contato" class="btn">Fale Conosco</a>
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero"
}
</script>

<style scoped>
.hero {
  height: 100vh;
  background: linear-gradient(120deg, #2d6cdf, #5b9cff);
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  padding: 20px;
}

.hero-content {
  max-width: 700px;
  animation: fade 1.2s ease;
}

.hero h1 {
  font-size: 48px;
  margin-bottom: 20px;
}

.hero p {
  font-size: 18px;
  margin-bottom: 30px;
  line-height: 1.6;
}

.btn {
  display: inline-block;
  background: white;
  color: #2d6cdf;
  padding: 14px 28px;
  border-radius: 6px;
  text-decoration: none;
  font-weight: bold;
  transition: 0.3s;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.2);
}

@keyframes fade {
  from {
    opacity: 0;
    transform: translateY(25px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* RESPONSIVIDADE */
@media (max-width: 768px) {

  .hero {
    height: auto;
    min-height: 100vh;
    padding: 120px 20px 80px;
  }

  .hero h1 {
    font-size: 32px;
    line-height: 1.2;
  }

  .hero p {
    font-size: 16px;
  }

  .btn {
    padding: 12px 22px;
    font-size: 14px;
  }
}

@media (max-width: 420px) {

  .hero h1 {
    font-size: 26px;
  }

  .hero p {
    font-size: 15px;
  }
}

</style>
