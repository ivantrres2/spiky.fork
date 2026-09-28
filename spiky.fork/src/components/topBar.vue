<template>
	<header class="top-bar">
		<a class="top-bar__brand" href="/" aria-label="Home">
			<slot name="logo"><img src="../assets/ceciarum-logo.svg" alt="Logo" style="width: 100px"></slot>
		</a>
        <p class="title">CECIA UPRM <span class="subtitle"><br>Capítulo Estudiantil del <br> Colegio de Ingenieros y Agrimensores de Puerto Rico</span></p>
		

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
	</header>
</template>

<style scoped>
.top-bar {
	align-items: center;
	background: #fff;
	border-bottom: 10px solid #266E49;
	display: flex;
	gap: 2rem;
	justify-content: space-between;
	padding: 0.25rem 2rem;
}

.top-bar__brand {
	color: #111827;
	font-size: 1.25rem;
	font-weight: 700;
	text-decoration: none;
}

.top-bar__nav {
	align-items: center;
	display: flex;
	gap: 1.5rem;
	margin-left: auto;
}

.top-bar__nav a {
	color: #4b5563;
	text-decoration: none;
}

.top-bar__nav a:hover,
.top-bar__nav a:focus-visible {
	color: #111827;
}

.top-bar__button {
	background: #111827;
	border-radius: 0.375rem;
	color: #fff;
	padding: 0.625rem 1rem;
	text-decoration: none;
}

@media (max-width: 640px) {
	.top-bar {
		gap: 1rem;
		padding: 0.875rem 1rem;
	}

	.top-bar__nav {
		display: none;
	}
}
</style>
