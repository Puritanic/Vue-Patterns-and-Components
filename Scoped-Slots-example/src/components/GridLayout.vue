<template>
	<div class="game-container flex flex-wrap -mx-4">
		<a href="#" v-for="game in games" :key="game.id" class="w-1/5 px-4 mb-12 no-underline">
			<img :src="game.cover.url.replace('t_thumb', 't_cover_big')" alt="cover">
			<div
				class="text-black font-semibold text-lg overflow-hidden whitespace-no-wrap overflow-dots"
			>{{ game.name }}</div>
			<div
				class="text-grey-darker text-base overflow-hidden whitespace-no-wrap overflow-dots pb-1"
			>{{ game.genres[0].name }}</div>
		</a>
	</div>
</template>

<script>
export default {
	props: ['games'],
};
</script>

