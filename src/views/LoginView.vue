<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import { useDisplay } from 'vuetify'
import { ref } from 'vue'

const rememberMe = ref(false) // Define the variable using ref
const { mobile } = useDisplay()
</script>

<template>
  <AppLayout>
    <template #content>
      <v-row class="d-flex justify-center mt-5">n
        <v-col cols="12" md="6" class="mx-auto">
          <v-card class="mx-auto" color="grey-lighten-1" rounded="lg" elevation="8">
            <template v-slot:title>
              <div class="text-center fs-5 mb-4" style="font-weight: bold; font-size: 2rem">
                CareLink
              </div>
            </template>

            <v-card-text class="bg-surface-light pt-4">
              <v-form fast-fail @submit.prevent>
                <p>ID Number:</p>
                <v-text-field
                  prepend-inner-icon="mdi-account"
                  label="Enter your ID number"
                  color="green"
                  placeholder="ID Number"
                ></v-text-field>

                <p>Password:</p>
                <v-text-field
                  prepend-inner-icon="mdi-lock"
                  label="Enter your password"
                  color="green"
                  placeholder="Password"
                  type="password"
                ></v-text-field>

                <v-checkbox label="Remember Me" v-model="rememberMe"></v-checkbox>

                <v-btn class="rounded-s-lg" type="submit" block color="green-darken-3"
                  >Log in</v-btn
                >
              </v-form>
              <v-divider class="my-5"></v-divider>
              <h5 class="text-center">
                Don't have an account?<router-link to="/register"
                  ><b> Click here to Register</b></router-link
                >
              </h5>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
