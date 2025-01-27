<script setup>
import { ref } from 'vue'

const visible = ref(false)
</script>

<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field placeholder="Email address" prepend-inner-icon="mdi-email-outline"></v-text-field>

    <v-text-field
      :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="visible ? 'text' : 'password'"
      placeholder="Enter your password"
      prepend-inner-icon="mdi-lock-outline"
      @click:append-inner="visible = !visible"
    ></v-text-field>

    <v-btn class="mt-2 bg-primary" type="submit" prepend-icon="mdi-login" block>Login</v-btn>
  </v-form>
</template>
