<template>
  <div>
    <router-link to="/about" class="mt-5 text-xl text-green-600 hover:underline"
      >Ir a about</router-link
    >
    <br />
    <h1>
      <br />
      <px-assets-table :assets="assets" />
    </h1>
  </div>
</template>

<script>
import api from "@/api";
import PxAssetsTable from "@/components/PxAssetsTable.vue";

export default {
  name: "Home",
  components: { PxAssetsTable },

  data() {
    return {
      assets: [],
    };
  },

  created() {
    api.getAssets().then((assets) => (this.assets = assets));
  },
};
</script>
