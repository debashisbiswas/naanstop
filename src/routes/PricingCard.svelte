<script lang="ts">
	export let header: string;
	export let priceDisplay: string;
</script>

<div class="card bg-base-100 text-center shadow-xl">
	<div class="card-body">
		<h2 class="text-xl">{header}</h2>
		<p class="my-3 text-5xl font-bold">{priceDisplay}</p>
	</div>
</div>
