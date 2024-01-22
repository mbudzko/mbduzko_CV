<script setup>
defineProps({
  title: {
    type: String,
    default: '',
  },
  linkedinLink: {
    type: String,
    default: '',
  },
  position: {
    type: String,
    default: '',
  },
  description: {
    type: String,
    default: '',
  },
  startDate: {
    type: String,
    default: '',
    // MMM yyyy
  },
  endDate: {
    type: String,
    default: 'Current',
    // MMM yyyy
  }
})
</script>

<template>
  <div class="card">
    <div class="header">
      <span class="title">
        <a
          v-if="linkedinLink"
          :href="linkedinLink"
          target="_blank"
        >{{ title }}</a>
        <span v-else>
          {{ title }}
        </span>
      </span>

      <span class="period">
        {{ startDate }} - {{ endDate }}
      </span>
    </div>

    <div class="position">
      <strong>Position:</strong> {{ position }}
    </div>

    <div class="description">
      <strong>Description:</strong> {{ description || '-' }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  padding: 1rem;
  border-left: 3px solid;
  margin-bottom: 1rem;
}

.header {
  font-size: large;
  padding-bottom: 0.5rem;
}

.title {
  font-weight: 700 !important;
}

.period {
  margin-left: 1rem;
  font-weight: 400;
}
</style>
