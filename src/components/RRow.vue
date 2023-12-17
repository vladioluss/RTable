<script>
import RCell from "@/components/RCell.vue";

export default {
  props: {
    item: {
      type: Object,
    },

    index: {
      type: Number,
    },
  },

  components: {
    RCell,
  },
}
</script>

<template>
  <div>
    <RCell>
      <slot
          name="cell"
          :item="item"
          :index="index"
      ></slot>
    </RCell>
  </div>
</template>

<style scoped>

</style>