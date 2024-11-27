<script setup>
import { ref } from 'vue'

const theme = ref('light')

function onClick () {
  theme.value = theme.value === 'light' ? 'dark' : 'light'
}
</script>

<template>
<v-responsive class="border rounded">
    <v-app :theme="theme">
      <v-app-bar class="px-3">
        <v-spacer></v-spacer>

        <v-btn
          :prepend-icon="theme === 'light' ? 'mdi-weather-sunny' : 'mdi-weather-night'"
          text="Toggle Theme"
          slim
          @click="onClick"
        ></v-btn>
      </v-app-bar>

      <v-main>
        <v-container>
         <v-row>
          <v-col cols="12" md="6" class="mx-auto"> 
            <v-card
    class="mx-auto"
    prepend-icon="$vuetify"
    subtitle="The #1 Vue UI Library"
    width="400"
  >
    <template v-slot:title>
      <span class="font-weight-black">Welcome to Vuetify</span>
    </template>

    <v-card-text class="bg-surface-light pt-4">
      <v-form fast-fail @submit.prevent>
                <v-text-field label="Role (Student/Staff)" variant="outlined"></v-text-field>
                <v-text-field label="ID Number" variant="outlined"></v-text-field>
                <v-text-field label="FirstName" variant="outlined"></v-text-field>
                <v-text-field label="LastName" variant="outlined"></v-text-field>
                <v-text-field label="Email" variant="outlined"></v-text-field>
                <v-text-field label="Phone Number" variant="outlined"></v-text-field>
                <v-text-field label="Password" type="password" variant="outlined"></v-text-field>
                <v-text-field label="Password Confirmation" type="password" variant="outlined">
                </v-text-field>
                <v-btn class="rounded-s-lg mt-2" type="submit" block color="green-darken-3">Register</v-btn>
              </v-form>
              <v-divider class="my-5"></v-divider>
              <h5 class="text-center">
                Already have an account?<RouterLink to="/login">Click here to Login</RouterLink>
              </h5>
    </v-card-text>
  </v-card>

          </v-col>
         </v-row>
        </v-container>
      </v-main>
      <v-footer class="text-center" color="yellow-accent-4" border app>
        <div class="text-center" style="width: 100%">
          2024 - CareLink University Booking Appointment
        </div>
      </v-footer>

    </v-app>
  </v-responsive>
</template>