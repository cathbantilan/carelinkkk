<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content
      ><v-row class="d-flex justify-center mt-5">
        <v-col cols="12" md="6" class="mx-auto">
          <v-card class="mx-auto" color="grey-lighten-1" rounded="lg" elevation="3">
            <template v-slot:title>
              <div class="text-center fs-5 mb-5" style="font-weight: bold; font-size: 2rem">
                Sign Up
              </div>
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
                Already have an account?<RouterLink to="/login"> Click here to Login</RouterLink>
              </h5>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </template>
  </AppLayout>
</template>
