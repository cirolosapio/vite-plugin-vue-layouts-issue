<template>
  <q-item clickable tag="a" target="_blank" :to="to">
    <q-item-section v-if="icon" avatar>
      <q-icon :name="icon" />
    </q-item-section>

    <q-item-section>
      <q-item-label>{{ to }}</q-item-label>
    </q-item-section>
  </q-item>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'EssentialLink',
  props: {
    to: {
      type: String,
      required: true,
    },

    icon: {
      type: String,
      default: '',
    },
  },
});
</script>
