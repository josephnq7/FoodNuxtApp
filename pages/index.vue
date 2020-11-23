<template>
  <main class="container">
    <AppHeader/>
    <AppRestaurantinfo />
  </main>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import AppRestaurantinfo from "@/components/AppRestaurantinfo.vue";

export default {
	components: {
		AppRestaurantinfo,
		AppHeader,
	},
}

</script>

<style>

</style>
