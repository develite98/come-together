<script lang="ts">
	export let index = 0;
	export let item: {
		title: string;
		date: Date;
		level: number;
		image: string;
		slots: number;
		joined: number;
	};

	const levels = ['Beginner', 'Average', 'Pro'];
	const levelColors = ['#0976D8', '#009E30', '#F27500'];

	const options: Intl.DateTimeFormatOptions = {
		weekday: 'long',
		year: 'numeric',
		month: 'long',
		day: 'numeric'
	};
</script>

<div class="flex flex-col items-start rounded-xl overflow-hidden bg-white shadow-lg mb-6 relative">
	<div
		class="absolute top-2 left-2 px-2 py-1 rounded-lg text-white min-w-10"
		style="background-color: {levelColors[item.level - 1]};"
	>
		Cấp {levels[item.level - 1]}
	</div>
	<div class="flex w-full items-center justify-center h-48 bg-gray-300 dark:bg-gray-700">
		{#if !item.image}
			<svg
				class="w-10 h-10 text-gray-200 dark:text-gray-600"
				aria-hidden="true"
				xmlns="http://www.w3.org/2000/svg"
				fill="currentColor"
				viewBox="0 0 16 20"
			>
				<path
					d="M14.066 0H7v5a2 2 0 0 1-2 2H0v11a1.97 1.97 0 0 0 1.934 2h12.132A1.97 1.97 0 0 0 16 18V2a1.97 1.97 0 0 0-1.934-2ZM10.5 6a1.5 1.5 0 1 1 0 2.999A1.5 1.5 0 0 1 10.5 6Zm2.221 10.515a1 1 0 0 1-.858.485h-8a1 1 0 0 1-.9-1.43L5.6 10.039a.978.978 0 0 1 .936-.57 1 1 0 0 1 .9.632l1.181 2.981.541-1a.945.945 0 0 1 .883-.522 1 1 0 0 1 .879.529l1.832 3.438a1 1 0 0 1-.031.988Z"
				/>
				<path d="M5 5V.13a2.96 2.96 0 0 0-1.293.749L.879 3.707A2.98 2.98 0 0 0 .13 5H5Z" />
			</svg>
		{:else}
			<img
				class="w-full h-full object-cover object-center"
				src={item.image + '?random=' + index}
				alt="img"
			/>
		{/if}
	</div>

	<div class="p-4">
		<h2 class="font-semibold text-gray-500">
			{item.date.toLocaleDateString('vi-VN', options)}
		</h2>

		<h1 class="text-2xl mt-1 font-medium">{item.title}</h1>

		<a href="#" class="flex items-center gap-2 mt-1 text-blue-600 dark:text-blue-500">
			<svg
				xmlns="http://www.w3.org/2000/svg"
				xmlns:xlink="http://www.w3.org/1999/xlink"
				width="16px"
				height="40px"
				viewBox="0 0 32 40"
				version="1.1"
			>
				<title>Location icon</title>
				<g id="Location-icon" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
					<g id="Icon/location" stroke="#979797" stroke-width="2">
						<path
							d="M31,15.6521739 C31,21.142785 25.8942068,28.767832 15.9992351,38.5940048 C6.10515545,28.7668795 1,21.1424421 1,15.6521739 C1,11.6085572 2.67716251,7.948794 5.38558566,5.29924962 C8.10205118,2.6418377 11.8553074,1 16,1 C20.1446926,1 23.8979488,2.6418377 26.6144143,5.29924962 C29.3228375,7.948794 31,11.6085572 31,15.6521739 Z M24,15 C24,12.790861 23.1045695,10.790861 21.6568542,9.34314575 C20.209139,7.8954305 18.209139,7 16,7 C13.790861,7 11.790861,7.8954305 10.3431458,9.34314575 C8.8954305,10.790861 8,12.790861 8,15 C8,17.209139 8.8954305,19.209139 10.3431458,20.6568542 C11.790861,22.1045695 13.790861,23 16,23 C18.209139,23 20.209139,22.1045695 21.6568542,20.6568542 C23.1045695,19.209139 24,17.209139 24,15 Z"
							id="Combined-Shape"
						/>
					</g>
				</g>
			</svg>

			Sân vận động Thống Nhất - Xem địa điểm
		</a>
	</div>

	<div class="w-full flex items-center p-4 gap-1">
		<div class="text-lg font-semibold flex gap-2 items-center">
			<span>{item.joined} / {item.slots}</span>
		</div>
		<button
			class="ml-auto text-white px-4 w-auto h-12 bg-second rounded-full touchable mouse shadow transition ease-in duration-200 focus:outline-none text-sm"
		>
			<span>Theo dõi</span>
		</button>

		<button
			class="text-white px-4 w-auto h-12 bg-primary rounded-full touchable mouse shadow transition ease-in duration-200 focus:outline-none text-sm"
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
	</div>
</div>
