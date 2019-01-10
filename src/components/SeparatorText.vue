<template>
	<v-text-field prepend-icon="text_fields" label="挿入文字" type="text" v-model="text">
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
			this.$emit('syncSeparator', this.text)
		}
	}
}
</script>
