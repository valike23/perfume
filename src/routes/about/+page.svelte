<script lang="ts">
	import { onMount } from 'svelte';
	import Footer from '$lib/Footer.svelte';
	import Header from '$lib/Header.svelte';
	import Bottom from '$lib/Bottom.svelte';
	let win: any = {};

	onMount(() => {
		win = window;
	});
</script>

<Header />

<section class="about_section layout_padding">
	<div class="container">
		<div class="row">
			<div class="col-md-6">
				<div class="detail-box">
					<div class="heading_container">
						<h2>About Our Product</h2>
					</div>
					<p>
						OIK perfumes Ltd is a company that operates from Dubai, UAE.<br/>
                         We produce fragrance of diverse range of luxurious fragrance for both men and women. Our perfumes are crafted with to the finest ingredients and are designed to calm your mind, lift your spirit, help in your stress control, boost your morale, makes you more attractive, some of the components enhance aromatherapy and reduce insomnia. These qualities are found in one type to the other, this you can see are you browse through our website
Our fragrance is a product of scientific research which makes it to be  amongst the highest quality you can find around the world.
As a growing company that reckon amongst the best fragrance products in the world we are gradually expanding in our distributorship in order to get the products closer to you.
					</p>
					<a href="/"> Read More </a>
				</div>
			</div>
			<div class="col-md-6">
				<div class="img-box">
					<img src="https://res.cloudinary.com/tjconnect/image/upload/v1679005059/products_xzvizr.jpg" alt="" />
				</div>
			</div>
		</div>
	</div>
</section>

   <Footer></Footer>
   <Bottom></Bottom>
