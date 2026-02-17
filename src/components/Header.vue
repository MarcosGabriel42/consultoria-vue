<template>
  <header class="header">
    <div class="container">

      <div class="logo">NovaEra</div>

      <div class="hamburger" @click="open = !open">
        ☰
      </div>

      <nav class="menu" :class="{ active: open }">
        <a href="#home" @click="open=false">Início</a>
        <a href="#sobre" @click="open=false">Sobre</a>
        <a href="#servicos" @click="open=false">Serviços</a>
        <a href="#contato" @click="open=false">Contato</a>
      </nav>

    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      open: false
    }
  }
}
</script>

<style scoped>
.header {
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  background: white;
  box-shadow: 0 2px 10px rgba(0,0,0,0.08);
  z-index: 1000;
}

/* container padrão */
.container {
  max-width: 1100px;
  margin: auto;
  padding: 18px 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* logo */
.logo {
  font-size: 22px;
  font-weight: bold;
  color: #2d6cdf;
}

/* MENU DESKTOP */
.menu {
  display: flex;
  align-items: center;
}

.menu a {
  margin-left: 25px;
  text-decoration: none;
  color: #333;
  font-weight: 500;
  transition: 0.3s;
}

.menu a:hover {
  color: #2d6cdf;
}

/* BOTÃO HAMBURGER */
.hamburger {
  display: none;
  font-size: 26px;
  cursor: pointer;
}

/* 📱 MOBILE */
@media (max-width: 768px) {

  .hamburger {
    display: block;
  }

  .menu {
    position: absolute;
    top: 70px;
    right: 0;
    background: white;
    width: 220px;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
    box-shadow: 0 10px 25px rgba(0,0,0,0.1);

    transform: translateX(100%);
    transition: transform 0.3s ease;
  }

  .menu a {
    margin: 12px 0;
  }

  .menu.active {
    transform: translateX(0);
  }
}
</style>
