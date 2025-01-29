<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import LoginForm from '@/components/auth/LoginForm.vue'
import { useDisplay } from 'vuetify'

const { mobile } = useDisplay()
</script>

<template>
  <AppLayout>
    <template #content>
      <v-container fluid>
        <v-row>
          <v-col cols="12" md="6" class="mx-auto pt-16"
            ><v-card class="mx-auto" elevation="24">
              <v-card-title class="text-center">
                <v-img
                  class="mx-auto"
                  src="/images/leave-logo.png"
                  :width="mobile ? '75vw' : '25vw'"
                  :height="mobile ? '75vw' : '25vw'"
                  cover
                  style="border-radius: 50%; object-fit: cover"
                ></v-img>

                <h3 class="font-weight-black text-center">Work Pause</h3>
                <p>Login Form</p>
                <v-divider class="my-2"></v-divider>
              </v-card-title>

              <v-card-text class="bg-surface-light pt-4">
                <LoginForm></LoginForm>

                <v-divider class="my-5"> </v-divider>
                <h5 class="text-center">
                  Don't have account?
                  <RouterLink class="text-primary font-weight-black" to="/register"
                    >Click here to Register!</RouterLink
                  >
                </h5>
              </v-card-text>
            </v-card></v-col
          >
        </v-row>
      </v-container>
    </template>
  </AppLayout>
</template>
