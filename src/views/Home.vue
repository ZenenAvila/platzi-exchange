<template>
  <div>
    <px-assets-table />
    <router-link to="/about" class="mt-5 text-xl text-green-600 hover:underline"
      >Ir a about</router-link
    >
  </div>
</template>

<script>
import PxAssetsTable from "@/components/PxAssetsTable.vue";

export default {
  name: "Home",
  components: { PxAssetsTable },
};
</script>
