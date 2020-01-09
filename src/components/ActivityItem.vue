<template>
  <div>
    <ActivityItemUpdate v-if="isUpdateActive" />
    <ActivityItemDetail v-else :activity="activity" :categories="categories" />
  </div>
</template>

<script>
import ActivityItemDetail from "./ActivityItemDetail";
import ActivityItemUpdate from "./ActivityItemUpdate";
export default {
  components: {
    ActivityItemDetail,
    ActivityItemUpdate
  },
  props: {
    activity: {
      required: true,
      type: Object
    },
    categories: {
      required: true,
      type: Object
    }
  },
  data() {
    return {
      isUpdateActive: false
    };
  }
};
</script>

<style scoped>
</style>