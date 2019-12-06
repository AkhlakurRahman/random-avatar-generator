<template>
	<div class="wrapper">
		<h3>Random Avatar Generator</h3>

		<div>
			<label for="avatarInput">Input:</label>
			<input type="text" v-on:input="onInput" id="avatarInput" />
		</div>

		<div class="output">
			Output:
			<div v-html="indenticon"></div>
		</div>
	</div>
</template>

<script>
import jdenticon from 'jdenticon';

export default {
	name: 'InputField',
	data() {
		return {
			avatar: ''
		};
	},
	computed: {
		indenticon() {
			if (this.avatar !== '') {
				return jdenticon.toSvg(this.avatar, 200);
			}
			return null;
		}
	},
	methods: {
		onInput: function(event) {
			this.avatar = event.target.value;
		}
	}
};
</script>

<style scoped>
.wrapper {
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}

h3 {
	margin: 50px 0;
}

label {
	margin-right: 10px;
}

.output {
	margin-top: 20px;
}
</style>
