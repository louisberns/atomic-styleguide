<template lang="html">
  <div class="page-header index-page container">
    <div class="page-header__info container column">
    	<!--<img class="page-header__img" :src="imgSRC" :alt="imgALT" v-if="imgSRC">-->
    	<slot name="image"></slot>
    	<h1 class="page-header__title"> {{ title }} </h1>
    </div>
  </div>
</template>

<script>
	import info from '@/static/data/info.json';

	export default {
		name: "indexImg",
		props: {
			title: {
				type: String
			},
			imgSRC: {
				type: String
			},
			imgALT: {
				type: String
			}
		},
		data() {
			return {
				info
			}
		}
	}
</script>

<style lang="scss" scoped>
	@import '../assets/css/base/variables.scss';

	.index-page {
		min-height: 40vh;
		width: 100%;
		background: $color-black;
		justify-content: center;
		align-items: center;
    margin: 0;

		.page-header__info {
			width: 100%;
			justify-content: center;
			align-items: center;

			.page-header__title {
				color: $color-secondary;
				text-align: center;
				margin: 20px 0;
			}

			.page-header__img {
				width: 100%;
				max-width: 180px;
				align-self: center;
				justify-self: center;
				margin: 20px 0;
			}
		}
	}
</style>
