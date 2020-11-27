<template>
	<main class="container restaurant">
		<div class="restaurantheading">
			<h1>Restaurants</h1>

			<AppSelect @change="selectedRestaurant = $event" />
		</div>

<!-- 		<pre>{{ $data }}</pre> -->
		
		<AppRestaurantinfo :datasource="filteredRestaurants"/>
	</main>
</template>

<script>
	import AppRestaurantinfo from "@/components/AppRestaurantinfo.vue";
	import AppSelect from "@/components/AppSelect.vue";
	import { mapState } from "vuex";

	export default {
		components: {
			AppRestaurantinfo,
			AppSelect,
		},
		data() {
			return {
				selectedRestaurant: ''
			}
		},
		computed: {
			...mapState(["fooddata"]),
			filteredRestaurants() {
				if (this.selectedRestaurant) {
					return this.fooddata.filter(el => {
						let name = el.name.toLowerCase();
						return name.includes(this.selectedRestaurant);
					});
				}

				return this.fooddata;
			}
		}
	};
</script>

<style lang="scss" scoped>
	
</style>