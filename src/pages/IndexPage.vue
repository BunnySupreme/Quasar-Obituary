<template>
  <q-page class="q-pa-md">
    <q-stepper
      v-model="step"
      vertical
      animated
    >
      <q-step
        :name="1"
        title="Personal Info"
        subtitle="Name and dates"
      >
        <q-stepper-navigation>
          <q-btn @click="step = 2" label="Next" color="primary"></q-btn>
        </q-stepper-navigation>
      </q-step>

      <q-step
        :name="2"
        title="Biography"
        subtitle="Life story"
      >
        <q-stepper-navigation>
          <q-btn flat @click="step = 1" label="Back"/>
          <q-btn @click="step = 3" label="Next" color="primary"/>
        </q-stepper-navigation>
      </q-step>

      <q-step :name="3" title="Template" subtitle="Choose a layout">
        <q-stepper-navigation>
          <q-btn flat @click="step = 2" label="Back" />
          <q-btn color="positive" label="Finish" />
        </q-stepper-navigation>
      </q-step>
    </q-stepper>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const step = ref(1)
</script>
