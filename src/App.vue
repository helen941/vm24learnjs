<script setup>
import { ref } from 'vue'
import Modal from './components/Modal.vue'

let modal1Active = ref(false);
let modal2Active = ref(false);
let modal3Active = ref(false);
</script>

<template>
  <div class="container mt-2">
    <div class="content">
      <button class="button is-primary" @click="modal1Active = true">Open Modal 1</button>
      <button class="button is-link" @click="modal2Active = true">Open Modal 2</button>
      <button class="button is-warning" @click="modal3Active = true">Open Modal 3</button>

      <Modal :active="modal1Active" @close="modal1Active = false" url="https://picsum.photos/1290/960?random=1"> </Modal>
      <Modal :active="modal2Active" @close="modal2Active = false" url="https://picsum.photos/1290/960?random=2"> </Modal>
      <Modal :active="modal3Active" @close="modal3Active = false" >
      <div class="card">
  <div class="card-content">
    <div class="content">
      Kass ehk kodukass on kaslaste sugukonna kassi perekonda kuuluv väike kiskja, kaslaste hulgas ainus koduloom. Kodukasse arvatakse maailmas elavat 600 miljonit ehk rohkem kui kõiki teisi kaslasi kokku.
    </div>
  </div>
</div>
      </Modal>
    
    </div>
  </div>
</template>