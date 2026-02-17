<template>
  <footer class="footer">
    <div class="container footer-content">

      <div class="footer-about">
        <h3 class="logo">NovaEra</h3>
        <p>
          Ajudando empresas a evoluírem através de estratégia,
          tecnologia e inovação.
        </p>
      </div>

      <div class="footer-links">
        <h4>Links rápidos</h4>
        <a href="#home">Início</a>
        <a href="#sobre">Sobre</a>
        <a href="#servicos">Serviços</a>
        <a href="#contato">Contato</a>
      </div>

      <div class="footer-social">
        <h4>Redes sociais</h4>
        <div class="icons">
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-linkedin-in"></i></a>
          <a href="#"><i class="fab fa-whatsapp"></i></a>
        </div>
      </div>

    </div>

    <div class="footer-bottom">
      © 2026 NovaEra Consultoria — Todos os direitos reservados
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
.footer {
  background: #111827;
  color: #e5e7eb;
  padding-top: 70px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
  padding-bottom: 40px;
}

.footer-about p {
  margin-top: 10px;
  line-height: 1.6;
  color: #cbd5e1;
}

.logo {
  color: #5b9cff;
}

.footer-links {
  display: flex;
  flex-direction: column;
}

.footer-links a {
  text-decoration: none;
  color: #cbd5e1;
  margin: 6px 0;
  transition: 0.3s;
}

.footer-links a:hover {
  color: #5b9cff;
}

.footer-social .icons a {
  display: inline-block;
  margin-right: 12px;
  font-size: 18px;
  color: #cbd5e1;
  transition: 0.3s;
}

.footer-social .icons a:hover {
  color: #5b9cff;
}

.footer-bottom {
  text-align: center;
  border-top: 1px solid #374151;
  padding: 18px;
  font-size: 14px;
  color: #9ca3af;
}

/* RESPONSIVO */
@media (max-width: 900px) {

  .footer-content {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 30px;
  }

  .footer-links,
  .footer-social {
    align-items: center;
  }

  .footer-links a {
    margin: 5px 0;
  }

  .footer-social .icons {
    margin-top: 10px;
  }
}

@media (max-width: 500px) {

  .footer {
    padding-top: 50px;
  }

  .footer-bottom {
    font-size: 12px;
    padding: 15px 10px;
  }
}

</style>
