<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import RegisterForm from '@/components/auth/RegisterForm.vue'
</script>

<template>
  <AppLayout>
    <template #content>
      <v-container fluid>
        <v-row>
          <v-col cols="12" md="6" class="mx-auto"
            ><v-card class="mx-auto" elevation="24">
              <v-img src="/images/leave-logo.png"> </v-img>
              <v-card-title class="text-center">
                <h3 class="font-weight-black text-center">Work Pause</h3>
                <p>Register Form</p>
                <v-divider class="my-2"></v-divider>
              </v-card-title>

              <v-card-text class="bg-surface-light pt-4">
                <RegisterForm></RegisterForm>
                <v-divider class="my-5"> </v-divider>
                <h5 class="text-center">
                  Already have account?
                  <RouterLink class="text-primary font-weight-black" to="/"
                    >Click here to Login!</RouterLink
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
