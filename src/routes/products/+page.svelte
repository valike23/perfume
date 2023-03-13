<script lang="ts">
	import Bottom from '$lib/Bottom.svelte';
	import Footer from '$lib/Footer.svelte';
	import Header from '$lib/Header.svelte';
	import Loading from '$lib/loading.svelte';
	import { onMount } from 'svelte';
	import axios from 'axios';
	import { APPLICATION_URL } from '$lib/properties/init';
	import type { Iproduct } from '$lib/properties/model';

	let loader = true;
	let products: Iproduct[] = [];

	onMount(async () => {
	try {
		const data = await axios.get(APPLICATION_URL + 'products');
		products = data.data;
		loader = false;
		console.log('products', products);
	} catch (error) {
		products =[];
		loader = false;
	}
		

	});
</script>

{#if loader}
	<Loading />
{/if}
<div class="hero_area pt-5 ">
	<Header />
</div>

<div class="container">
	<h1 class="text-center my-5">Product List</h1>
	<div class="row">
		{#each products as product}
		<div class="col-md-4 col-12">
			<div class="card mb-4">
				<img
					src="{product.image}"
					class="card-img-top"
					alt="{product.slug}"
				/>
				<div class="card-body">
					<h5 class="card-title">{product.name}</h5>
					<p class="card-text" style=" white-space: nowrap; overflow: hidden; text-overflow: ellipsis;">
						<small>{product.description}</small>
					</p>
					<p class="card-text">Rating: 4.5 (10 reviews)</p>
					<h6 class="card-subtitle mb-2 text-muted">${product.price}</h6>
					<a href="#" class="btn btn-primary">Add to Cart</a>
				</div>
			</div>
		</div>
		{/each}
	</div>
</div>

<Footer />
<Bottom />
