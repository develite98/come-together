<script lang="ts">
	import '../app.scss';
	import { App } from 'konsta/svelte';
</script>

<App theme="material" safeAreas dark={true}>
	<slot />
</App>

<style lang="scss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>
