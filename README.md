# Amazônia Palace Resort

O **Amazônia Palace Resort** é uma aplicação One Page desenvolvida em Vue.js, criada para apresentar um resort amazônico fictício com foco em experiência, comodidades, galeria visual e reserva.  
O projeto foi construído com componentes reutilizáveis, estilização própria e comportamento interativo, mantendo uma estrutura simples, organizada e totalmente alinhada ao propósito da aplicação.

---

## Visão Geral

A aplicação apresenta o resort em uma única página, dividida em seções:

- **Hero** com imagem principal e chamada de destaque  
- **O Hotel** com descrição institucional  
- **Comodidades** utilizando cards reutilizáveis  
- **Galeria** com imagens do resort  
- **Formulário de Reserva** com campos reativos  
- **Rodapé** estilizado  

Tudo foi desenvolvido com **Vue.js + Vite**, utilizando apenas recursos nativos da linguagem e **CSS puro**, sem frameworks externos.

---

## Componentes da Aplicação

A aplicação utiliza quatro componentes principais, todos com `<script setup>`:

### MenuSuperior.vue  
Menu fixo com navegação por scroll suave entre as seções da página.

### InfoCard.vue  
Card reutilizável para exibir as comodidades do resort.  
Recebe props (`titulo` e `descricao`) e é usado várias vezes com conteúdos diferentes.

### FormularioReserva.vue  
Formulário interativo com campos reativos (`ref()`), validação simples e mensagem dinâmica exibida após a reserva.

### Rodape.vue  
Rodapé simples com estilização própria.

---

## Funcionalidades Implementadas

- Navegação suave entre seções  
- Cards reutilizáveis com props  
- Formulário com reatividade (`ref()` e `v-model`)  
- Mensagem dinâmica após envio  
- Galeria responsiva  
- Ícones representados por símbolos Unicode (🛖 💆 🌊 🍽️)  
- Animações suaves de entrada (fade)  
- Layout totalmente responsivo  
- Estilização própria com CSS puro  

---

## Tecnologias Utilizadas

- **Vue.js 3**  
- **Vite**  
- **JavaScript**  
- **CSS puro**  
- **HTML**  

Sem uso de bibliotecas externas de interface ou frameworks CSS.

---

## Estrutura do Projeto

src/
 ├── components/
 │    ├── MenuSuperior.vue
 │    ├── InfoCard.vue
 │    ├── FormularioReserva.vue
 │    └── Rodape.vue
 ├── App.vue
 └── main.js

---

## Repositório no GitHub

Repositório público contendo o projeto completo e o README com os prompts utilizados:

https://github.com/vazmerces-thay/amazonia_palace_resort

---

## Prompts Utilizados

O desenvolvimento do Amazônia Palace Resort começou com a busca por um nome que representasse um hotel sofisticado na Amazônia. A partir disso, foram solicitadas ideias para criação de uma logo e variações em tons de verde, mantendo a identidade visual conectada à natureza. Em seguida, houve o pedido para gerar uma imagem inicial do hotel, representando chalés em área verde, piscina, contato com animais, um lago amplo e uma área para passeio a cavalo, que serviria como destaque visual do site. Também foram discutidas formas de apresentar as comodidades, como o uso de quadrados ou círculos com elementos como sustentabilidade e serviços premium, acompanhados de descrições. A estrutura inicial da página foi enviada, incluindo a posição da logo, o menu com seções como O resort, localização, comodidades, contato e área do cliente, além do slogan e da chamada de hospedagem. Foram definidos textos introdutórios sobre o resort e, por fim, solicitada a criação da área de reserva com campos para entrada, saída, quantidade de hóspedes, crianças e opção de transfer. Esses prompts orientaram toda a construção da aplicação, desde o conceito visual até a funcionalidade final.

