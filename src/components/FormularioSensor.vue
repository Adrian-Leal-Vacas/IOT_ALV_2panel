<script setup>
import { ref, defineProps } from 'vue'
import { updateData } from '@/firebase'
const referencia = 'IOT_ALV'
const props = defineProps(['idActivo', 'nombreSensor', 'estadoSensor'])
const valor = ref(props.estadoSensor)
// Función de cuando dejas de escribir que te realiza los cambios y lo actualiza en firebase
const submitForm = () => {
  updateData(props.idActivo, referencia, {
    [props.nombreSensor]: valor.value
  })
}
</script>
<template>
  <form class="mb-5 text-base" @submit.prevent="submitForm">
    <label for="valor">Lectura del sensor: {{ props.nombreSensor }}</label>
    <input
      class="text-black"
      type="number"
      v-model="valor"
      id="valor"
      name="valor"
      @input="submitForm"
    />
  </form>
</template>
<style lang="scss" scoped></style>
