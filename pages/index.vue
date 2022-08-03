<template>
  <div>
    <custom-form />
  </div>
</template>

<script>
import customForm from '../components/custom-form.vue'
import customTable from '../components/custom-table.vue'
export default {
  name: 'indexPage',
  components: {
    customForm,
    customTable
  }
}
</script>
