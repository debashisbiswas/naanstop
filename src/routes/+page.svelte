<script lang="ts">
	import Heading from './Heading.svelte';
	import MenuItem from './MenuItem.svelte';
	import PricingCard from './PricingCard.svelte';

	let organicChickenSelected = false;

	interface Option {
		servings: number;
		basePrice: number;
		organicPrice: number;
	}

	const options: Option[] = [
		{
			servings: 4,
			basePrice: 52,
			organicPrice: 62
		},
		{
			servings: 8,
			basePrice: 104,
			organicPrice: 124
		},
		{
			servings: 12,
			basePrice: 144,
			organicPrice: 172
		}
	];
</script>

<div class="my-16 grid w-full place-items-center">
	<div class="w-4/5 max-w-screen-lg">
		<div class="mb-12 text-5xl font-bold tracking-tight">NaanStop</div>

		<div class="mb-12">
			<Heading>Menu</Heading>

			<div class="grid gap-6 md:grid-cols-2">
				<MenuItem
					name="Butter Chicken"
					imageSource="https://source.unsplash.com/Xnb826JWdDI"
					description="Chicken breast, yellow onion, tomato, yogurt, oil, milk cream, ginger, garlic, kasoori methi, salt, red chilli powder"
				/>

				<MenuItem
					name="Cauliflower Rainbow Veg"
					imageSource="https://source.unsplash.com/MRHyv-hHxgk"
					description="Cauliflower, carrots, peas, tomato, oil, mustard, cumin, coriander powder, salt, tumeric"
				/>

				<MenuItem
					name="French beans"
					imageSource="https://source.unsplash.com/64_w-cfxua4"
					description="Green beans, potatoes, onions, tomatoes, garlic, green chilli, coriander powder, oil, mustard seeds, salt, tumeric"
				/>

				<MenuItem
					name="Rice"
					imageSource="https://source.unsplash.com/xmuIgjuQG0M"
					description="Basmati rice, salt"
				/>
			</div>
		</div>

		<div>
			<Heading>Pricing</Heading>

			<div class="text-center">
				<label class="mb-4 flex cursor-pointer items-center justify-center">
					<input
						type="checkbox"
						bind:checked={organicChickenSelected}
						class="checkbox-primary checkbox mx-2"
					/>
					<div class="text-lg">Organic Chicken (add 20%)</div>
				</label>

				<div class="mb-12 grid gap-8 md:grid-cols-3">
					{#each options as option}
						<PricingCard
							header="{option.servings} servings"
							price={organicChickenSelected ? option.organicPrice : option.basePrice}
						/>
					{/each}
				</div>

				<button class="btn-primary btn-lg btn">Order now</button>
			</div>
		</div>
	</div>
</div>
