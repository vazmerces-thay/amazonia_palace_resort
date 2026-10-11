<template>
<section class="reserva">
  <h2 class="titulo">Reserve sua experiência</h2>

  <form class="form-grid">

    <div class="campo">
      <label>Data de entrada</label>
      <input type="date" v-model="entrada" />
    </div>

    <div class="campo">
      <label>Data de saída</label>
      <input type="date" v-model="saida" />
    </div>

    <div class="campo">
      <label>Hóspedes</label>
      <input type="number" min="1" v-model="hospedes" />
    </div>

    <div class="campo">
      <label>Crianças</label>
      <input type="number" min="0" v-model="criancas" />
    </div>

    <div class="campo">
      <label>Transfer</label>
      <select v-model="transfer">
        <option>Sim</option>
        <option>Não</option>
      </select>
    </div>

    <div class="campo">
      <label>Email para envio das informações</label>
      <input type="email" v-model="email" placeholder="seuemail@email.com" />
    </div>

  </form>

  <button class="botao" @click.prevent="reservar">Confirmar Reserva</button>

  <p v-if="mensagem" class="mensagem">{{ mensagem }}</p>
</section>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const entrada = ref('')
const saida = ref('')
const hospedes = ref(1)
const criancas = ref(0)
const transfer = ref('Não')
const mensagem = ref('')

function reservar() {
if (!email.value || !entrada.value || !saida.value) {
  mensagem.value = "Por favor, preencha o email, data de entrada e saída."
  return
}

mensagem.value =
  `Reserva confirmada! As informações de valores e pagamento serão enviadas para o email ${email.value}.`
}
</script>

<style scoped>
.reserva {
background-color: #0F2E1D;
color: #D4A94A;
padding: 2rem;
border-radius: 12px;
margin-top: 2rem;
}

.titulo {
text-align: center;
margin-bottom: 1.5rem;
font-size: 1.6rem;
}

.form-grid {
display: grid;
grid-template-columns: repeat(2, 1fr);
gap: 1.2rem;
margin-bottom: 1.5rem;
}

.campo {
display: flex;
flex-direction: column;
gap: 0.4rem;
}

input,
select {
padding: 0.7rem;
border-radius: 6px;
border: none;
background-color: #D4A94A;
color: #0F2E1D;
font-weight: bold;
}

input::placeholder {
color: #0F2E1D;
opacity: 0.8;
}

.botao {
width: 100%;
background-color: #D4A94A;
color: #0F2E1D;
border: none;
padding: 0.9rem;
cursor: pointer;
border-radius: 8px;
font-size: 1.1rem;
font-weight: bold;
transition: 0.3s;
}

.botao:hover {
background-color: #EBCB6A;
}

.mensagem {
margin-top: 1rem;
text-align: center;
font-size: 1.1rem;
}

@media (max-width: 600px) {
.form-grid {
  grid-template-columns: 1fr;
}
}
</style>
