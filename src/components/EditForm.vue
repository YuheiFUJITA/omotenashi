<template>
  <v-form>
    <input-text v-on:syncText="syncText"/>
    <separator-text v-on:syncSeparator="syncSeparator"/>
  </v-form>
</template>

<script>
import InputText from "./InputText";
import SeparatorText from "./SeparatorText";

export default {
  components: {
    InputText,
    SeparatorText
  },
  data() {
    return {
      text: "",
      separator: "",
      result: ""
    };
  },
  methods: {
    syncText: function(text) {
			this.text = text
		},
		syncSeparator: function(separator) {
			this.separator = separator
		},
		generateResult: function() {
			this.result = this.text.replace(/(.)(?=.)/g, "$1" + this.separator)
			alert(this.result)
		}
  }
};
</script>
