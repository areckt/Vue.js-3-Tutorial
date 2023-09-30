<script setup>
defineProps({
  text: {
    type: String,
    required: true
  }
})
</script>

<template>
  <button>{{ text }}</button>
</template>

<style scoped>
button {
  cursor: pointer;
	min-width: 150px;
	max-width: 250px;
	position: relative;

	margin: 1em 2em;
	padding: 1em 2em;

	border: none;
	background: none;
	color: inherit;
  font-weight: 600;
	
	z-index: 1;

	-webkit-transition: color 0.3s;
	transition: color 0.3s;
	-webkit-transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
	transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
}

button::before, button::after {
  content: '';
	position: absolute;
	background: var(--color-blue-gray-300);
	z-index: -1;
  -webkit-transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
	transition-timing-function: cubic-bezier(0.2, 1, 0.3, 1);
}

button::before {
  top: -4px;
	bottom: -4px;
	left: -4px;
	right: -4px;
	opacity: 0.2;
  border-radius: 8px;
	-webkit-transform: scale3d(0.7, 1, 1);
	transform: scale3d(0.7, 1, 1);
	-webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
	transition: transform 0.3s, opacity 0.3s;
}

button::after {
  top: 0;
	left: 0;
	width: 100%;
	height: 100%;
  border-radius: 6px;
	-webkit-transform: scale3d(1.1, 1, 1);
	transform: scale3d(1.1, 1, 1);
	-webkit-transition: -webkit-transform 0.3s, background-color 0.3s;
	transition: transform 0.3s, background-color 0.3s;
}

button:hover {
  color: #fff;
}

button:hover::before {
  opacity: 1;
}

button:hover::after {
  background-color: var(--color-blue-gray-800);
}

button:hover::after,
button:hover::before {
	-webkit-transform: scale3d(1, 1, 1);
	transform: scale3d(1, 1, 1);
}
</style>