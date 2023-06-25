<script lang="ts">
	export let name: string;
	export let description: string;
	export let imageSource: string;
</script>

<div class="grid">
	<div class="card bg-base-100 shadow-xl">
		<figure>
			<img src={imageSource} alt={name} class="h-48 w-full object-cover" />
		</figure>
		<div class="card-body">
			<h2 class="card-title">{name}</h2>
			<p>{description}</p>
		</div>
	</div>
</div>
