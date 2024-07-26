<script setup>

import { onMounted } from 'vue'

onMounted(() => {     

	$('.homepage-slides').owlCarousel({
		items: 1,
		dots: false,
		nav: true,
		loop: true,
		autoplay: true,
		autoplayTimeout: 5000,
		smartSpeed: 2000,
		slideSpeed: 600,
		animateOut: 'fadeOut',
		navText: ["<i class='la la-angle-left'></i>", "<i class='la la-angle-right'></i>"],
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 1,
				nav: false,
				dots: false,
			},
			768: {
				items: 1,
				nav: false,
				dots: false,
			},
			1100: {
				items: 1,
				nav: true,
				dots: false,
			}
		}
	});


	$(".homepage-slides").on("translate.owl.carousel", function () {
		$(".single-slide-item h1").removeClass("animated fadeInUp").css("opacity", "1");
		$(".single-slide-item h6").removeClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item p").removeClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item a.main-btn").removeClass("animated fadeInDown").css("opacity", "1");
	});

	$(".homepage-slides").on("translated.owl.carousel", function () {
		$(".single-slide-item h1").addClass("animated fadeInUp").css("opacity", "1");
		$(".single-slide-item h6").addClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item p").addClass("animated fadeInDown").css("opacity", "1");
		$(".single-slide-item a.main-btn").addClass("animated fadeInDown").css("opacity", "1");
	});
  
});

</script>

<template>
    <div>
 		<!----div class="hero-area-bg-2">
 			<div ></div>
 			<div class="hero-area-content">
 				<div class="container">
 					<div class="row justify-content-center">
 						<div class="col-lg-12 wow fadeInUp animated" data-wow-delay=".2s">
 							<div class="section-title">
								<img class="robot-logo" src="/assets/img/robot-flotante.png" alt="">
 								<h1 class="h1-azul">IMPULSA TUS VENTAS<br></h1>
								<h3 class="h3-negro">Lleva tu negocios al siguiente nivel</h3>
 								<p class="p-negro"> Industrial Revolution, in modern history, the process of change from an agrarian <br>and handicraft economy to one dominated by industry and machine manufacturing.</p>
								 <button  class="botom-azul">Registrate</button>
 							</div>
 							
 						</div>
 					</div>
 				</div>
 			</div>
 		</div> ---->

 		<div class="single-slide-item hero-area-bg-2">
 			<div></div>
 			<div class="hero-area-content">
 				<div class="container">
 					<div class="row justify-content-center">
 						<div class="col-lg-12 wow fadeInUp animated" data-wow-delay=".2s">
 							<div class="section-title">
								<img class="robot-logo" src="/assets/img/robot-flotante.png" alt="">
								<h1 class="h1-azul">IMPULSA TUS VENTAS<br></h1>
								<h3 class="h3-negro">Lleva tu negocios al siguiente nivel</h3>
								<p class="p-negro"> Industrial Revolution, in modern history, the process of change from an agrarian <br>and handicraft economy to one dominated by industry and machine manufacturing.</p>
 							</div>
							 <button  class="botom-azul">Registrate</button>
 						</div>
 					</div>
 				</div>
 			</div>
 		</div> 
 	</div>
</template>

<style scoped>
  @media (max-width: 767px) {
            .h1-azul {
                font-size: 30px;
				color: 	#1E90FF;
				top: -170px;
				right: 80px; 
                /* Otros estilos específicos para teléfonos */
            }
			.robot-logo {
    position: absolute;
    top: -170px;
    right: -10px; /* Ajusta este valor para mover la imagen más a la derecha */
    width: 30%;
}
.h3-negro{
	color: #000;
	top: -200px;
    right: 70px; /* Ajusta este valor para mover la imagen más a la derecha */
}
.p-negro{
	color: #000;
	top: -150px;
    right: 50px; /* Ajusta este valor para mover la imagen más a la derecha */
}
.botom-azul{
	width: 40%;
  background-color: white;
  color: black;
  border: 2px solid #1e90ff;;
  padding: 10px 20px; /* Ajusta el tamaño del botón */
  font-size: 16px; /* Ajusta el tamaño del texto */
  border-radius: 5px; /* Opcional: para bordes redondeados */
  cursor: pointer; /* Cambia el cursor al pasar sobre el botón */
}
		}






		@media (min-width: 768px) {
            .h1-azul {
                font-size: 60px;
                /* Otros estilos específicos para computadoras */
            }
            .h1-azul{
	font-size: 60px;
	color: 	#1E90FF;
	top: -120px;
    right: 50px; /* Ajusta este valor para mover la imagen más a la derecha */
}
.robot-logo {
    position: absolute;
    top: -100px;
    right: -30px; /* Ajusta este valor para mover la imagen más a la derecha */
    width: 40%;
}
.h3-negro{
	color: #000;
	top: -150px;
    right: 50px; /* Ajusta este valor para mover la imagen más a la derecha */
}
.p-negro{
	color: #000;
	top: -120px;
    right: 50px; /* Ajusta este valor para mover la imagen más a la derecha */
}
.botom-azul{
	width: 15%;
  background-color: white;
  color: black;
  border: 2px solid #1e90ff;;
  padding: 10px 20px; /* Ajusta el tamaño del botón */
  font-size: 16px; /* Ajusta el tamaño del texto */
  border-radius: 5px; /* Opcional: para bordes redondeados */
  cursor: pointer; /* Cambia el cursor al pasar sobre el botón */
}

        }

</style>