<template>
  <BoxWrapper>
    <Input v-model="inputValue" />
    <PasswordTest :password-strength="inputValue" />
  </BoxWrapper>
</template>

<script setup>
import { ref } from 'vue';
import Input from '@/components/Input.vue'
import PasswordTest from '@/components/PasswordTest.vue'
import BoxWrapper from '@/components/BoxWrapper.vue'

const inputValue = ref(String());
</script>

<style scoped></style>
