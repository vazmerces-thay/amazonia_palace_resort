<template>
<MenuSuperior />

<section id="hero" class="fade hero">
  <img :src="imagemPrincipal" class="hero-img" />
  <div class="hero-text">
    <h1>Seu refúgio exclusivo na Amazônia</h1>
    <p>Experiências únicas em meio à floresta.</p>
  </div>
</section>

<section id="hotel" class="fade hotel">
  <h2>O Hotel</h2>

  <p>
    O Amazônia Palace Resort é o primeiro hotel‑resort totalmente integrado à natureza,
    oferecendo uma experiência única em meio à floresta amazônica. Aqui, cada detalhe foi
    pensado para proporcionar conforto, tranquilidade e conexão com o ambiente natural.
    Nosso serviço de transfer exclusivo garante uma chegada prática e segura, levando você
    diretamente ao coração da Amazônia.
    <br><br>
    Chalés sofisticados, gastronomia regional, atividades ao ar livre e experiências
    sensoriais fazem parte da nossa essência. No Amazônia Palace Resort, você vive dias de
    descanso, contemplação e bem‑estar, cercado pela maior floresta tropical do mundo.
  </p>
</section>

<section id="comodidades" class="fade comodidades">
  <h2>Comodidades</h2>

  <div class="grid">
    <InfoCard
      v-for="(item, i) in comodidades"
      :key="i"
      :titulo="item.titulo"
      :descricao="item.descricao"
    />
  </div>
</section>

<section id="galeria" class="fade galeria">
  <h2>Galeria</h2>

  <div class="mosaico">
    <img src="https://i.postimg.cc/7Z8JLV6Y/Piscina.png" class="foto" />
    <img src="https://i.postimg.cc/FH5kKZRK/Quarto.png" class="foto" />
    <img src="https://i.postimg.cc/P5svq4xN/Rio.png" class="foto" />
    <img src="https://i.postimg.cc/y843NPd1/Hotel.png" class="foto" />
    <img src="https://i.postimg.cc/t4Qng5Tj/Banheiro.png" class="foto" />
  </div>
</section>

<section id="reserva" class="fade">
  <FormularioReserva />
</section>

<Rodape />
</template>

<script setup>
import MenuSuperior from './components/MenuSuperior.vue'
import InfoCard from './components/InfoCard.vue'
import FormularioReserva from './components/FormularioReserva.vue'
import Rodape from './components/Rodape.vue'

const imagemPrincipal = "https://i.postimg.cc/8zQfCH51/Hotel-2.png"

const comodidades = [
{ 
  titulo: '🛖 Hospedagem Premium',
  descricao: 'Chalés luxuosos com vista para o lago.'
},
{ 
  titulo: '💆 Spa Amazônico',
  descricao: 'Massagens e terapias naturais.'
},
{ 
  titulo: '🌊 Piscina Infinita',
  descricao: 'Vista para o lago e bar molhado.'
},
{ 
  titulo: '🍽️ Gastronomia Amazônica',
  descricao: 'Sabores locais e menu gourmet.'
}
]
</script>

<style scoped>
.fade {
opacity: 0;
transform: translateY(20px);
animation: fadeIn 1.2s forwards;
}

@keyframes fadeIn {
to {
  opacity: 1;
  transform: translateY(0);
}
}

.hero {
position: relative;
}

.hero-img {
width: 100%;
height: 450px;
object-fit: cover;
filter: brightness(70%);
}

.hero-text {
position: absolute;
top: 30%;
left: 50%;
transform: translateX(-50%);
color: white;
text-align: center;
font-size: 1.4rem;
}

.hotel,
.comodidades,
.galeria {
padding: 2rem;
background-color: #1A3B28;
color: #D4A94A;
line-height: 1.6;
font-size: 1.1rem;
}

.mosaico {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
gap: 12px;
}

.foto {
width: 100%;
border-radius: 8px;
object-fit: cover;
transition: 0.3s;
}

.foto:hover {
transform: scale(1.03);
}

.grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
gap: 1rem;
}

@media (max-width: 600px) {
.hero-img {
  height: 300px;
}

.hero-text {
  font-size: 1rem;
  top: 35%;
}

.hotel,
.comodidades,
.galeria {
  padding: 1.2rem;
  font-size: 1rem;
}
}
</style>
