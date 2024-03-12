<template>
<form>
  Create user form
  <BaseInput
    type="text"
    :value="user.firstName"
    @input="onPayload"
    @change="onPayload"
  />
</form>
</template>

<script lang="ts" setup>
import BaseInput from '@/components/BaseInput.vue'
const user = ref({
  firstName: 'firstName',
  lastName: 'lastName',
})
const onPayload = (payload) => {
  console.log({ payload });
}
</script>
