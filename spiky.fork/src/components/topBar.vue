<template>
	<header class="top-bar">

		<a class="top-bar__brand" href="/" aria-label="Home">
			<img class="cecia" src="../assets/ceciarum-logo.svg" alt="Logo">
		</a>
		<div class="title-subtitle-container">
        <p class="title">CECIA UPRM </p>
		<p class="subtitle"><br>Capítulo Estudiantil del 
			<br> Colegio de Ingenieros y Agrimensores de Puerto Rico
			<br>Universidad de Puerto Rico - Mayagüez</p>
		</div>
		

		
<nav class="top-bar__nav" aria-label="Main navigation">
  <RouterLink
    v-for="page in visiblePages"
    :key="page.path"
    :to="page.path"
  >
    {{ page.name }}
  </RouterLink>
</nav>


		<div class="menu">
		<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" height="50px" width="50px" fill="#266E49"><path d="M3,18V16H21v2H3Zm0-5V11H21v2H3ZM3,8V6H21V8H3Z"/></svg>
		</div>

		<div class="header-low-poly">
			<img src="../assets/header-low-poly.svg" alt="Logo">
		</div>


	</header>
</template>


<script setup>

import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const pages = [
  { name: 'Inicio', path: '/' },
  { name: 'Anuncios', path: '/news' },
  { name: 'Acerca de', path: '/about' },
  { name: 'Únete!', path: '/join' }
]

const visiblePages = computed(() => {
  return pages.filter(page => page.path !== route.path)
})


</script>
