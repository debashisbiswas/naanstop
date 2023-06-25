<script lang="ts">
	import { fly } from 'svelte/transition';

	export let header: string;
	export let price: number;
</script>

<div class="card bg-base-100 text-center shadow-xl">
	<div class="card-body">
		<h2 class="text-xl mb-3">{header}</h2>
		{#key price}
			<p class="text-5xl font-bold" in:fly={{ y: -16 }}>${price}</p>
		{/key}
	</div>
</div>
