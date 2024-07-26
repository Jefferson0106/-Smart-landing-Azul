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
    <div class="achievement-area">
 		
      <h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2>
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
.title {
	text-align: center;
            top: 50px;
            left: 43%;
            transform: translateX(-50%);
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
        }
      }
</style>