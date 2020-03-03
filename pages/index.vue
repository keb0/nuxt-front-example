<template>
  <v-row>
    <v-col md="4" sm="12">
      <v-form>
        <v-row>
          <v-col md="12">
            <v-combobox
              v-model="select"
              :items="items"
              label="Sort"
              outlined
            ></v-combobox>
          </v-col>
          <v-col md="12">
            <v-card outlined tile>
              <v-card-text>detail</v-card-text>
              <v-combobox
                v-model="select"
                :items="items"
                label="Category"
                prepend-inner-icon="fa-home"
                outlined
              ></v-combobox
              ><v-text-field
                v-model="brand"
                label="Brand"
                prepend-inner-icon="fa-home"
                outlined
              ></v-text-field>
              <v-card class="d-flex flex-row flex-wrap">
                <v-checkbox
                  v-model="checkbox"
                  class="px-2"
                  label="Do you agree?"
                ></v-checkbox>
                <v-checkbox
                  v-model="checkbox"
                  class="px-2"
                  label="Do you agree?"
                ></v-checkbox>
                <v-checkbox
                  v-model="checkbox"
                  class="px-2"
                  label="Do you agree?"
                ></v-checkbox>
              </v-card>
              <v-card class="d-flex flex-row justify-space-around">
                <v-btn>Submit</v-btn>
                <v-btn>Reset</v-btn>
              </v-card>
            </v-card>
          </v-col>
        </v-row>
      </v-form>
    </v-col>

    <v-col md="8" sm="12">
      <v-card outlined tile><v-card-text>main</v-card-text></v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      items: ['Programming', 'Design', 'Vue', 'Vuetify']
    }
  }
}
</script>
