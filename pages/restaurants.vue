<template>
	<main class="container restaurant">
		<div class="restaurantheading">
			<h1>Restaurants</h1>

			<AppSelect @change="selectedRestaurant = $event" />
		</div>

<!-- 		<pre>{{ $data }}</pre> -->
		
		<AppRestaurantinfo />
	</main>
</template>

<script>
	import AppRestaurantinfo from "@/components/AppRestaurantinfo.vue";
	import AppSelect from "@/components/AppSelect.vue";
	export default {
		components: {
			AppRestaurantinfo,
			AppSelect,
		},
		data() {
			return {
				selectedRestaurant: ''
			}
		}
	};
</script>

<style lang="scss" scoped>
	
</style>