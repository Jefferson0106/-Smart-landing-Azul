<script setup>
import { onMounted, ref } from "vue";
import axios from "axios";

const projects = ref([]);

onMounted(async () => {
  const { data: fetchedProjects } = await axios.get("/data/projects.json");
  projects.value = fetchedProjects.projects;
});


</script>
<template>
		<div class="single-slide-item">
            
		<!---h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2> ------>
        <h2 class="title">¡Regístrate ahora y dale un nuevo enfoque a tu negocio!</h2> 
        <form class="form-overlay">
			<div class="kimber">
				<input type="text" id="name" name="name" placeholder="Nombre completo">
				<input type="email" id="email" name="email" placeholder="Correo electrónico"><br><br>
                <input type="text" id="phone" name="phone" placeholder="Teléfono"><br><br>
                <input type="text" id="company" name="company" placeholder="Empresa"><br><br>
                <textarea id="message" name="message" placeholder="Mensaje [opcional]"></textarea><br><br>
                <button type="button" class="azul">Comienza Ahora</button>
			</div>
        </form>
    </div>
</template>


<style scoped>

@media (max-width: 767px) {
    .form-overlay{ 
        position: absolute;
            top: 60%;
            left: 50%;
            transform: translate(-50%, -50%);
        background-color: #FFFFFF; /* Fondo semitransparente */
            padding: 10px;
            border-radius: 1px;
            width: 80%; /* Ajusta el ancho según sea necesario */
            box-shadow: 0 4px 8px black;
    }
    

   /* Estilo para los campos de entrada, elementos select y áreas de texto */
input[type="text"], select, textarea {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    resize: vertical;
}

/* Estilo para las etiquetas que se muestran junto a los campos */
label {
    padding: 12px 12px 12px 0;
    display: inline-block;
}

/* Estilo para el botón de envío */
input[type="submit"] {
    background-color: #04AA6D;
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    float: right;
}

/* Estilo para el contenedor del formulario */
.container {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
}

/* Columna flotante para las etiquetas: ancho del 25% */
.col-25 {
    float: left;
    width: 25%;
    margin-top: 6px;
}

/* Columna flotante para los campos de entrada: ancho del 75% */
.col-75 {
    float: left;
    width: 75%;
    margin-top: 6px;
}

/* Limpieza de flotantes después de las columnas */
.row:after {
    content: "";
    display: table;
    clear: both;
}
title {
	text-align: center;
            top: 100px;
            left: 3%;
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
        }
        }


        @media (min-width: 768px) {
            .form-overlay {
            position: absolute;
            top: 41%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #FFFFFF; /* Fondo semitransparente */
            padding: 20px;
            border-radius: 10px;
            width: 80%; /* Ajusta el ancho según sea necesario */
            box-shadow: 0 4px 8px black;
        }

        .form-overlay h2 {
            text-align: center;
            color: #007BFF; /* Color del texto del encabezado */
        }

        .form-overlay label {
            display: block;
            margin-bottom: 5px;
            color: black;
        }

        .form-overlay input[type="text"],
        .form-overlay input[type="email"],
        .form-overlay textarea {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            color: black; 
        }
.azul{
	      width: 30%;
            padding: 10px;
			top: 10px;
            background-color: #FFFFFF ;
            color: black;
			border: 1px solid #1e90ff;
            border-radius: 5px;
            cursor: pointer;
			margin: 0 auto; 
  display: block;
}

.title {
	text-align: center;
            top: -90px;
            left: 50%;
            transform: translateX(-50%);
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
        }

/*.title {
	text-align: center;
            top: -50px;
            left: 50%;
            transform: translateX(-50%);
            color: #FFFFFF; 
            background-color: transparent;
            padding: 5px;
            border-radius: 5px;
            white-space: nowrap; 
        } */

        }
</style>