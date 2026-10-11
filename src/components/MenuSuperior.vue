<template>
<nav class="menu">
  <img :src="logo" alt="Logo do Amazônia Palace Resort" class="logo" />

  <ul>
    <li @click="scrollTo('hotel')">O Hotel</li>
    <li @click="scrollTo('comodidades')">Comodidades</li>
    <li @click="scrollTo('galeria')">Galeria</li>
    <li @click="scrollTo('reserva')">Reserva</li>
  </ul>
</nav>
</template>

<script setup>
const logo = "https://i.postimg.cc/HkD8L2xd/Logo.png"

function scrollTo(section) {
document.getElementById(section)?.scrollIntoView({ behavior: "smooth" })
}
</script>

<style scoped>
.menu {
background-color: #0F2E1D;
color: #D4A94A;
display: flex;
align-items: center;
justify-content: space-between;
padding: 1rem 2rem;
position: sticky;
top: 0;
z-index: 10;
}

.menu ul {
display: flex;
gap: 1.5rem;
list-style: none;
}

.menu li {
cursor: pointer;
transition: 0.3s;
}

.menu li:hover {
color: #EBCB6A;
}

.logo {
height: 60px;
}

@media (max-width: 600px) {
.menu ul {
  gap: 0.8rem;
  font-size: 0.8rem;
}
}
</style>
