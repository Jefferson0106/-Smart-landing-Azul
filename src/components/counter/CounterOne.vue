<script setup>

import { onMounted, ref, onUpdated } from 'vue'

import axios from "axios";

const counter = ref([]);

onMounted(async () => {
  const { data: fetchedCounter } = await axios.get("/data/counter.json");
  counter.value = fetchedCounter.counter;
});

onUpdated(() => {     
    $(".counter-number span").counterUp({
		delay: 10,
		time: 1000,

	});
  
});

</script>


<template>
   <div>
  <img src="/assets/img/fondo-footer.png" alt="Fondo de pie de página">
  <!---h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2> ---->
</div>
</template>


<style scoped>
@media (max-width: 767px) {
  title {
	text-align: center;
            top: 300px;
            left: 3%;
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
        }
}


@media (min-width: 768px) {
  .container {
    display: flex; /* Centrar horizontalmente */
    justify-content: center; /* Centrar horizontalmente */
    align-items: center; /* Centrar verticalmente */
    position: relative;
    text-align: center;
    color: white;
  }

  /* Texto centrado */
  .title {
    position: absolute;
    top: 10px;
    left: 50px;
  
    background-color: transparent;
    padding: 5px;
    border-radius: 5px;
    white-space: nowrap;
  }
}
</style>