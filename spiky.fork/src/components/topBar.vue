<template>
	<header class="top-bar">

		
		<a class="top-bar__brand" href="/" aria-label="Home">
			<slot name="logo"><img src="../assets/ceciarum-logo.svg" alt="Logo" style="width: 100px"></slot>
		</a>
		<div class="title-subtitle-container">
        <p class="title">CECIA UPRM </p>
		<p class="subtitle"><br>Capítulo Estudiantil del 
			<br> Colegio de Ingenieros y Agrimensores de Puerto Rico
			<br>Universidad de Puerto Rico - Mayagüez</p>
		</div>
		

		<nav class="top-bar__nav" aria-label="Main navigation">
			<slot name="navigation">
				<a href="#features">Link 1</a>
				<a href="#about">Link 2</a>
				<a href="#contact">Link 3</a>
			</slot>
		</nav>

		<div class="top-bar__actions">
			<slot name="actions">
				<a class="top-bar__button" href="#get-started">Button 1</a>
			</slot>
		</div>
		<div class="header-low-poly">
		<img src="../assets/header-low-poly.svg" alt="Logo">
		</div>
	</header>
</template>
