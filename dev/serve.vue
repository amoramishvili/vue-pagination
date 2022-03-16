<script lang="ts">
import { defineComponent } from "vue";
import VPagination from "@/pagination.vue";

export default defineComponent({
  name: "ServeDev",
  components: {
    VPagination,
  },
  setup() {
    const PaginationHandler = (pageNum: Number) => {
      console.log(pageNum);
    };

    return {
      PaginationHandler,
    };
  },
});
</script>

<template>
  <div id="app">
    <VPagination
      class="pagination"
      :pageRange="10"
      prevClass="prev"
      nextClass="next"
      nextText=""
      prevText=""
      :pageCount="{ autoCount: false, limit: 10, count: 20 }"
      :selectedPage="1"
      :clickHandler="PaginationHandler"
    />
  </div>
</template>
