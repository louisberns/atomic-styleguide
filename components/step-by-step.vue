<template lang="html">
	<div>
		<div v-if="itemsList && img" v-for="items in dataItems">
			<h3> {{ title }} </h3>
			<p> {{ message }} </p>
			<ul>
				<li v-for="i in itemsList"> {{ itemsList }} </li>
			</ul>
			<img src=" {{ img }} " alt="">
		</div>
		<div v-else-if="img">
			<h3> {{ title }} </h3>
			<p> {{ message }} </p>
			<img src=" {{ img }} " alt="">
		</div>
	</div>
</template>

<script>

	export default {
		props: {
			title: {
				type: String
			},
			message: {
				type: String
			},
			itemsList: {
				type: Array
			},
			dataItems: {
				type: Array
			}
		}
	}
</script>

<style lang="scss" scoped>
	
</style>