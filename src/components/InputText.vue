<template>
	<v-text-field prepend-icon="text_fields" label="テキスト" type="text" v-model="text">
	</v-text-field>
</template>

<script>
export default {
	data () {
		return {
			text: ''
		}
	},
	watch: {
		text () {
			this.$emit('syncText', this.text)
		}
	}
}
</script>
