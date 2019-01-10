<template>
  <v-app id="inspire">
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title>お・も・て・な・し</v-toolbar-title>
              </v-toolbar>
              <v-card-text>
								<edit-form ref="form"/>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn color="primary" @click="clickBtn">おもてなす</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import EditForm from './components/EditForm'

export default {
	components: {
		EditForm,
	},
  data: () => ({
    drawer: null
  }),

  props: {
    source: String
	},
	methods: {
		clickBtn: function() {
			this.$refs.form.generateResult()
		}
	}
};
</script>