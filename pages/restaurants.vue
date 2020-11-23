<template>
	<main class="container restaurant">
		<h1>Restaurants</h1>
		<AppRestaurantinfo />
	</main>
</template>

<script>
	import AppRestaurantinfo from "@/components/AppRestaurantinfo.vue";
	export default {
		components: {
			AppRestaurantinfo,
		},
	};
</script>

<style lang="scss" scoped>
	
</style>