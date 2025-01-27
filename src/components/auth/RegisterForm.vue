<script setup>
import { ref } from 'vue'

const visible = ref(false)
const confirmPasswordVisible = ref(false)
</script>

<template>
  <v-form fast-fail @submit.prevent>
    <v-row>
      <v-col cols="12" sm="6">
        <v-text-field label="Firstname"></v-text-field>
      </v-col>

      <v-col cols="12" sm="6">
        <v-text-field label="Lastname"></v-text-field>
      </v-col>
    </v-row>

    <v-text-field label="Email"></v-text-field>

    <v-text-field
      :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="visible ? 'text' : 'password'"
      placeholder="Password"
      prepend-inner-icon="mdi-lock-outline"
      @click:append-inner="visible = !visible"
    ></v-text-field>

    <v-text-field
      :append-inner-icon="confirmPasswordVisible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="confirmPasswordVisible ? 'text' : 'password'"
      placeholder="Password Confirmation"
      prepend-inner-icon="mdi-lock-outline"
      @click:append-inner="confirmPasswordVisible = !confirmPasswordVisible"
    ></v-text-field>

    <v-btn class="mt-2 bg-primary" type="submit" prepend-icon="mdi-account-plus" block
      >Register</v-btn
    >
  </v-form>
</template>
