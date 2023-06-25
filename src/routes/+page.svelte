<script>
	import MenuItem from './MenuItem.svelte';
	import PricingCard from './PricingCard.svelte';

	let organicChickenSelected = false;
</script>

<div class="mt-16 grid w-full place-items-center">
	<div class="w-4/5 space-y-8">
		<div class="text-5xl font-bold tracking-tight">NaanStop</div>

		<h2 class="text-3xl">Menu</h2>

		<div class="grid grid-cols-2 gap-6">
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

		<h2 class="text-3xl">Pricing</h2>

		<div class="mb-4">
			<label class="flex cursor-pointer items-center">
				<input
					type="checkbox"
					bind:checked={organicChickenSelected}
					class="checkbox-primary checkbox mx-2"
				/>
				<span class="text-lg">Organic Chicken (additional 20%)</span>
			</label>

			<div class="grid grid-cols-3 gap-8">
				<PricingCard header="4 servings" priceDisplay="$52" />
				<PricingCard header="8 servings" priceDisplay="$104" />
				<PricingCard header="12 servings" priceDisplay="$144" />
			</div>
		</div>

		<button class="btn-primary btn">Order now</button>
	</div>
</div>
