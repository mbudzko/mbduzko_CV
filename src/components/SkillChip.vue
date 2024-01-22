<template>
  <div class="chip">
    <span>{{ label }}</span>
  </div>
</template>

<script setup>
defineProps({
  label: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
@media (prefers-color-scheme: dark) {
  .chip {
    border: 1px solid #ccc;
    background-color: #242424;
    color: #ccc;
  }
  .chip:hover {
    background-color: #464646;
    color: #eaeaea;
  }
}

@media (prefers-color-scheme: light) {
  .chip {
    border: 1px solid #242424;
    background-color: #ffffff;
    color: #242424;
  }
  .chip:hover {
    background-color: #e5e5e5;
    color: #171717;
  }
}

.chip {
  display: inline-block;
  padding: 0.25rem 1rem;
  margin: 0.2rem;
  border-radius: 1rem;
  cursor: default;
  transition: background-color 0.3s;
}
</style>
