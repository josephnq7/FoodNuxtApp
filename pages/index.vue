<template>
  <main class="container">
    <AppHeader/>
    <AppRestaurantinfo :datasource="fooddata"/>
  </main>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import AppRestaurantinfo from "@/components/AppRestaurantinfo.vue";
import { mapState } from "vuex";

export default {
	components: {
		AppRestaurantinfo,
		AppHeader,
	},
	computed: {
		...mapState(["fooddata"]),
	},
};

</script>

<style>

</style>
