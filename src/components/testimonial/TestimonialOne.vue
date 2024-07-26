<script setup>

import { onMounted, onUpdated, ref } from "vue";
import axios from "axios";

const testimonials = ref([]);

onMounted(async () => {
  const { data: fetchedTestimonials } = await axios.get("/data/testimonials.json");
  testimonials.value = fetchedTestimonials.testimonials;
});

onUpdated(() => {     

    $('.testimonial-carousel').owlCarousel({
		items: 1,
		margin: 30,
		dots: true,
		nav: false,
		loop: true,
		autoplay: true,
		responsiveClass: true,
		responsive: {
			575: {
				items: 1,
				nav: false,
				dots: false,
			},

			767: {
				items: 2,
				nav: false
			},

			990: {
				items: 2,
				loop: true,

			},
			1200: {
				items: 3,
				dots: true,
				loop: true,
			}
		}
	});

  
});

</script>


<template>
	<div class="single-slide-item">
		<div>
				<h1 class="faq">FAQ</h1>
				<p class="faque">Lorem ipsum dolor sit amet consectetur,atior gdr erys sikkza </p>

					<img class="robo3" src="/assets/img/rob-logo.png" alt="">
					<img class="mensaje3" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span>

					<img class="mensaje4" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto1">Lorem ipsum dolor sit amet</h6>
					<span class="signo1">^</span>

					<img class="mensaje5" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto2">Lorem ipsum dolor sit amet</h6>
					<span class="signo2">^</span>

					<img class="mensaje6" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto3">Lorem ipsum dolor sit amet</h6>
					<span class="signo3">^</span>

					<!---img class="mensaje7" src="/assets/img/mensaje.png" alt="">
					<h6 class="texto4">Lorem ipsum dolor sit amet</h6>
					<span class="signo">^</span> --->

			</div>
			
	</div>
  </template>
  
  <style scoped>
@media (max-width: 767px) {
	.robo3{
	width: 40%;
	position: relative;
            left: -100px; 
            top: 10px;  
			margin: 20px;
        }
.faq{
	position: relative;
            left: -160px; 
            top: 40px;  
			margin: 20px;
			color: #FFFFFF;
}
.faque{
	position: relative;
            left: -70px; 
            top: 20px;  
			margin: 50px;
			color: #FFFFFF;
}
.mensaje3{
	width: 50%;
	position: relative;
            left: 100px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -200px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje4{
	width: 50%;
	position: relative;
	left: 100px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -650px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje5{
	width: 50%;
	position: relative;
	left: 100px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -730px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}.mensaje6{
	width: 50%;
	position: relative;
	left: 100px; /* Ajusta este valor para mover la imagen horizontalmente */
	top: -930px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 30px;
}
.mensaje7{
	width: 50%;
	position: relative;
            left: 430px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -730px;  /* Ajusta este valor para mover la imagen verticalmente */
			
}
.texto {
	font-size: 14px;
             position: absolute;
			left: 700px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: 230px;  /* Ajusta este valor para mover la imagen verticalmente */
            color: black;
        }
.texto1{
	position: relative;
			left: 800px; 
            top: -970px; 
            color: black;
}
.texto2{
	position: relative;
			left: 810px; 
            top: -1330px; 
            color: black;
}
.texto3{
	position: relative;
			left: 800px; 
            top: -1650px; 
            color: black;
}
.texto4{
	position: relative;
			left: 100px; 
            top: -1999px; 
            color: brown;
}
		.signo {
            position: absolute;
            top: 35%;
            left: 74%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
        }
		.signo1{
			position: absolute;
            top: 14%;
            left: 88%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
		}
		.signo2{
			position: absolute;
            top: 21%;
            left: 88%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
		}
		.signo3{
			position: absolute;
            top: 29%;
            left: 87%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
		}

}





@media (min-width: 768px) {
	.robo3{
	width: 40%;
	position: relative;
            left: 10px; 
            top: 10px;  
			margin: 20px;
        }
.faq{
	position: relative;
            left: 70px; 
            top: 40px;  
			margin: 20px;
			color: #FFFFFF;
}
.faque{
	position: relative;
            left: 50px; 
            top: 20px;  
			margin: 50px;
			color: #FFFFFF;
}
.mensaje3{
	width: 30%;
	position: relative;
            left: 100px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -300px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje4{
	width: 30%;
	position: relative;
            left: 670px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -660px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}
.mensaje5{
	width: 30%;
	position: relative;
            left: 670px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -1020px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 50px;
}.mensaje6{
	width: 30%;
	position: relative;
            left: 700px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -1360px;  /* Ajusta este valor para mover la imagen verticalmente */
			margin: 30px;
}
.mensaje7{
	width: 30%;
	position: relative;
            left: 430px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -190px;  /* Ajusta este valor para mover la imagen verticalmente */
			
}
.texto {
            position: relative;
			left: 800px; /* Ajusta este valor para mover la imagen horizontalmente */
            top: -650px;  /* Ajusta este valor para mover la imagen verticalmente */
            color: black;
        }
.texto1{
	position: relative;
			left: 800px; 
            top: -970px; 
            color: black;
}
.texto2{
	position: relative;
			left: 810px; 
            top: -1330px; 
            color: black;
}
.texto3{
	position: relative;
			left: 800px; 
            top: -1650px; 
            color: black;
}
.texto4{
	position: relative;
			left: 100px; 
            top: -1999px; 
            color: brown;
}
		.signo {
            position: absolute;
            top: 8%;
            left: 78%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
        }
		.signo1{
			position: absolute;
            top: 16%;
            left: 78%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
		}
		.signo2{
			position: absolute;
            top: 23%;
            left: 78%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
		}
		.signo3{
			position: absolute;
            top: 30%;
            left: 78%;/* Ajusta esta distancia según sea necesario */
            transform: translate(-50%, -50%);
            font-size: 40px; /* Ajusta el tamaño del signo según sea necesario */
            color: #1E90FF;
		}
}

 
	</style>
