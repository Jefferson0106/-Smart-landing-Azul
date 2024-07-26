<script setup>

import { onMounted, ref, onUpdated } from 'vue'

import axios from "axios";

const services = ref([]);

onMounted(async () => {
  const { data: fetchedServices } = await axios.get("/data/services.json");
  services.value = fetchedServices.services;
});

onUpdated(() => {     

		// Service Slider    
        $(".service-slider").owlCarousel({
		loop: true,
		items: 3,
		dots: true,
		nav: false,
		smartSpeed: 1000,
		autoHeight: false,
		touchDrag: true,
		mouseDrag: true,
		margin: 30,
		autoplay: true,
		slideSpeed: 600,
		responsive: {
			0: {
				items: 1,
				nav: false,
				dots: false,
			},
			600: {
				items: 2,
				nav: false,
				dots: false,
			},
			768: {
				items: 2,
				nav: false,
				dots: false,
			},
			1100: {
				items: 3,
				nav: false,
				dots: true,
			}
		}
	});
  
});

</script>

<template>
	<div class="project-bg">
		<div class="about-area section-padding">
 		<div class="container">
			<h2 class="h2-titulo"><span class="punto"></span>Gestiona Tus Productos y Servicios</h2>
 			<div class="row align-items-center">
 				<div class="col-lg-6 col-md-12 col-sm-12">
					<div class="about-img-wrap">
                    <div class="image-one wow fadeInUp" data-wow-delay=".2s" style="visibility: visible; animation-delay: 0.2s; animation-name: fadeInUp;">
						<!----h2 class="h2-titulo"><span class="punto"></span>Atencion Al Cliente Automatizada</h2> --->
                    </div>                        
                    <div class="image-two wow fadeInUp" data-wow-delay=".4s" style="visibility: visible; animation-delay: 0.4s; animation-name: fadeInUp;">
                        <!---img src="/assets/img/about/about-page-2.jpg" alt=""> --->
                    </div>                                            
                </div> 					
 				</div>
 				<div class="col-lg-6 col-md-12 col-sm-12">
 					<div>
 						<div class="section-title">
 							
							<img class="telefono" src="/assets/img/caja.png" alt="">
 						</div>
 						<p class="p-texto">We are build construction site lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea enim et, similique minus soluta ipsum dolor sit, amet .</p>
 					
</div>
 				</div>

 			</div>
 		</div>
 	</div>
     
	</div>
</template>

<style scoped>
 @media (max-width: 767px) {
	.h1-texto{
	text-align: center;
	top: -80px;
	margin: 20px;
}
.telefono{
	width: 90%;
	top: -260px;
    right: 0;
	
	
}
.h2-titulo{
	color: #1e90ff;
	display: flex;
        align-items: center;
		font-size: 30px;
	margin: 1px;
}
.punto {
        width: 30px;
        height: 20px;
        background-color: #1e90ff;
        border-radius: 50%;
        margin-right: 10px;
    }
	.section-title h2 {
		display: inline;
	}
	.p-texto{
		color: #000;
		
	}
		}



		@media (min-width: 768px) {
			.h1-texto{
	text-align: center;
	top: -80px;
	margin: 30px;
}
.telefono{
	position: relative;
	width: 100%;
	top: -200px;
    right: 0;
	
	
}
.h2-titulo{
	color: #1e90ff;
	display: flex;
        align-items: center;
		font-size: 30px;
	margin: 1px;
}
.punto {
        width: 30px;
        height: 20px;
        background-color: #1e90ff;
        border-radius: 50%;
        margin-right: 10px;
    }
	.section-title h2 {
		display: inline;
	}
	.p-texto{
		top: -560px;
		right: 600px;
	}
            }
</style>