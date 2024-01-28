<script lang="ts">
	import EventCard from '$lib/components/event-card.svelte';

	let data = [
		{
			title: 'Giao hữu bóng rổ HCMC',
			date: new Date(),
			level: 1,
			image: 'https://loremflickr.com/320/320/basketball/all',
			slots: 20,
			joined: 8
		},
		{
			title: 'Tranh cúp bóng rổ HCMC',
			date: new Date(),
			level: 3,
			image: 'https://loremflickr.com/320/320/basketball/all',
			slots: 11,
			joined: 2
		},
		{
			title: 'Luyện tập bóng rổ HCMC',
			date: new Date(),
			level: 2,
			image: 'https://loremflickr.com/320/320/basketball',
			slots: 15,
			joined: 7
		}
	];
</script>

<div class="p-4 !pt-4 w-full home">
	<div
		class="login-banner flex flex-col items-center justify-center rounded-xl overflow-hidden bg-white shadow-lg mb-8 p-4 mt-2"
	>
		<h2 class="text-xl font-semibold mb-2">Chào bạn mới</h2>
		<span class="w-3/4 text-center mb-2">Tìm kiếm, tham gia trận đấu, sảng khoái bung sức mình</span
		>
		<button
			class="text-white px-4 w-auto h-12 bg-primary rounded-lg touchable mouse shadow transition ease-in duration-200 focus:outline-none"
		>
			<span>Đăng nhập </span>
		</button>
	</div>
	<div class="font-bold mb-2 ml-2">Gợi ý gần bạn</div>
	{#each data as item, index}
		<EventCard {item} {index}></EventCard>
	{/each}
</div>

<!-- <div class="w-screen flex justify-center gap-2 items-center fixed bottom-5 right-0">
	<button
		class="text-white px-4 w-auto h-12 bg-second rounded-full touchable mouse shadow transition ease-in duration-200 focus:outline-none"
	>
		<span>Theo dõi</span>
	</button>

	<button
		class="text-white px-4 w-auto h-12 bg-primary rounded-full touchable mouse shadow transition ease-in duration-200 focus:outline-none"
	>
		<svg viewBox="0 0 20 20" enable-background="new 0 0 20 20" class="w-6 h-6 inline-block">
			<path
				fill="#FFFFFF"
				d="M16,10c0,0.553-0.048,1-0.601,1H11v4.399C11,15.951,10.553,16,10,16c-0.553,0-1-0.049-1-0.601V11H4.601
							C4.049,11,4,10.553,4,10c0-0.553,0.049-1,0.601-1H9V4.601C9,4.048,9.447,4,10,4c0.553,0,1,0.048,1,0.601V9h4.399
							C15.952,9,16,9.447,16,10z"
			/>
		</svg>
		<span>Tham gia</span>
	</button>
</div> -->

<style lang="scss">
	.login-banner {
		height: 200px;
		background-image: url('https://png.pngtree.com/thumb_back/fh260/background/20220217/pngtree-colorful-sports-theme-background-material-image_944423.jpg');
		background-size: cover;
	}
</style>
