<template>
	<div id="app">
		<InputField />
	</div>
</template>

<script>
import InputField from './components/InputField.vue';

export default {
	name: 'app',
	components: {
		InputField
	}
};
</script>

<style>
* {
	margin: 0;
	padding: 0;
}

#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	background: #eee;
	height: 100vh;
}
</style>
