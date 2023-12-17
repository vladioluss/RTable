<script>
import RRow from "@/components/RRow.vue";

export default {
  components: {
    RRow,
  },

  data() {
    return {
      items: [
        { value: 'Ячейка 1' },
        { value: 'Ячейка 2' },
      ],
    }
  },
}
</script>

<template>
  <div>
    <RRow
        v-for="(item, index) in items"
        :key="index"
        :item="item"
        :index="index"
    >
      <template #cell="{ item, index }">
        <p>index: {{ index }}</p>
        <p>value: {{ item.value }}</p>
      </template>
    </RRow>
  </div>
</template>

<style scoped>

</style>