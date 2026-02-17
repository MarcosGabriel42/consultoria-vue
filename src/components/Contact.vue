<template>
  <section id="contato" class="contact">
    <div class="container">

      <h2>Entre em Contato</h2>
      <p class="subtitle">
        Tem alguma dúvida ou quer falar com a nossa equipe?
        Envie uma mensagem para nós.
      </p>

      <form class="contact-form" @submit.prevent="sendMessage">
        <div class="input-group">
          <input type="text" placeholder="Seu nome" v-model="form.name" required>
          <input type="email" placeholder="Seu email" v-model="form.email" required>
        </div>

        <input type="text" placeholder="Assunto" v-model="form.subject" required>

        <textarea rows="5" placeholder="Sua mensagem..." v-model="form.message" required></textarea>

        <button type="submit">Enviar mensagem</button>

        <p class="success" v-if="sent">
          Mensagem enviada com sucesso! ✔
        </p>
      </form>

    </div>
  </section>
</template>

<script>
export default {
  name: "Contact",
  data() {
    return {
      sent: false,
      form: {
        name: "",
        email: "",
        subject: "",
        message: ""
      }
    }
  },
  methods: {
    sendMessage() {
      this.sent = true

      // limpa o formulário
      this.form = {
        name: "",
        email: "",
        subject: "",
        message: ""
      }
    }
  }
}
</script>

<style scoped>
.contact {
  padding: 120px 20px;
  background: #f5f7fb;
  text-align: center;
}

.contact h2 {
  font-size: 36px;
  color: #2d6cdf;
  margin-bottom: 10px;
}

.subtitle {
  color: #555;
  margin-bottom: 40px;
}

.contact-form {
  max-width: 650px;
  margin: auto;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.input-group {
  display: flex;
  gap: 15px;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 14px;
  border-radius: 8px;
  border: 1px solid #ddd;
  font-size: 15px;
  transition: 0.2s;
}

.contact-form input:focus,
.contact-form textarea:focus {
  border-color: #2d6cdf;
  outline: none;
  box-shadow: 0 0 0 2px rgba(45,108,223,0.15);
}

button {
  background: #2d6cdf;
  color: white;
  border: none;
  padding: 14px;
  border-radius: 8px;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #1f4fb0;
}

.success {
  margin-top: 10px;
  color: green;
  font-weight: bold;
}

/* RESPONSIVO */
@media (max-width: 768px) {

  .contact {
    padding: 90px 20px;
  }

  .input-group {
    flex-direction: column;
    gap: 12px;
  }

  .contact-form {
    width: 100%;
  }

  .contact-form input,
  .contact-form textarea {
    font-size: 14px;
    padding: 12px;
  }

  button {
    width: 100%;
    font-size: 15px;
    padding: 13px;
  }
}

</style>
