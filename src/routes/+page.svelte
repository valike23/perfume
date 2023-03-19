<script lang="ts">
	import Header from '$lib/Header.svelte';
	import { onMount } from 'svelte';
	import Footer from '$lib/Footer.svelte';
	import axios from 'axios';
	import { APPLICATION_URL } from '$lib/properties/init';
	import type { Iproduct } from '$lib/properties/model';
	let win: any = {};
	let perfumes: Iproduct[] = [];
	let mymap: any = {};
	const loadMap = () => {
		try {
			console.log('loading map');
			mymap = win.L.map('mapid').setView([25.2048, 55.2708], 3);
			// Create a marker for Dubai Mall
			const dubaiMallMarker = win.L.marker([25.2695591, 55.3326311]).addTo(mymap);

			dubaiMallMarker.bindPopup(`
  									<div class="popup-content">
    									<img style="width:100%; height:120px" src="https://source.unsplash.com/400x400/?dubai-mall" class="popup-image" />
   									 <div class="popup-text">
     								 <p><strong>Dubai Shop</strong></p>
     								 <p>Suite 16, Al Sudair Business Centre,
               							 Al Khabeesi Buildings, Plot 490-0
               							 Salahudeen Street, Opposite Danube Showroom 
               							 Dubai, UAE
									</p>
    								</div>
 									</div>
								`);
			const tanzaniaMaker = win.L.marker([-1.3827772, 36.9368036]).addTo(mymap);

			tanzaniaMaker.bindPopup(`
						  <div class="popup-content">
							<img style="width:100%; height:120px" src="https://lh5.googleusercontent.com/p/AF1QipPY8nfzhH3WZqswiwhdhrahHsTAYbV8QAZ1Svvx=w408-h544-k-no" class="popup-image" />
							<div class="popup-text">
						  <p><strong>Kenya Shop</strong></p>
						  <p>Greatwall Apartments , Beijing Road along Mombasa Road  Kenya
						</p>
						</div>
						 </div>
					`);
					const kenyaMarker = win.L.marker([-6.8331529, 39.2734326]).addTo(mymap);

kenyaMarker.bindPopup(`
			  <div class="popup-content">
				<img style="width:100%; height:120px" src="https://source.unsplash.com/400x400/?dubai-mall" class="popup-image" />
				<div class="popup-text">
			  <p><strong>Tanzania Shop</strong></p>
			  <p>House number 38,Mapinduzi street 
                Opposite Mlimani city,Sinza A,Dar es salaam, Tanzania
			</p>
			</div>
			 </div>
		`);
			win.L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
				attribution:
					'Map data &copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors, <a href="https://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>',
				maxZoom: 18
			}).addTo(mymap);
		} catch (error) {
			console.log(error);
		}
	};

	onMount(async () => {
		win = window;
		loadMap();
		try {
			const data = await axios.get(APPLICATION_URL + 'products/top_3');
			if (data) {
				perfumes = data.data;
			}
		} catch (error) {
			console.log(error);
			perfumes = [];
		}
	});
</script>

<svelte:head>
	<title>Oik Perfume - Buy the Best Perfumes Online | Free Shipping</title>
	<meta property="og:title" content="Oik Perfume - Buy the Best Perfumes Online | Free Shipping" />
	<meta
		property="og:description"
		content="Shop the best perfumes online at Oik Perfume. Browse our selection of fragrances and find your perfect scent today. Free shipping on orders over $50."
	/>
	<meta property="og:image" content="https://www.oik-perfumes.com/logo.png" />
	<meta property="og:url" content="https://www.oik-perfumes.com/" />
	<link rel="stylesheet" href="leaflet/leaflet.css" />
	<script src="leaflet/leaflet.js"></script>
</svelte:head>
<div class="hero_area pt-5 ">
	<!-- header section strats -->
	<Header />
	<!-- end header section -->
	<!-- slider section -->
	<section class="slider_section">
		<div class="side-img">
			<img src="images/side-img.png" alt="" />
		</div>
		<div class="container">
			<div class="row">
				<div class="col-md-6">
					<div class="detail-box">
						<h2>Body Spray</h2>
						<h1>
							O<span>I</span>K
						</h1>
						<a href="/"> Read More </a>
					</div>
				</div>
				<div class="col-md-6">
					<div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
						<div class="carousel-inner">
							<div class="carousel-item active">
								<div class="img-box">
									<img src="images/oik2.png" alt="" />
								</div>
							</div>
							<div class="carousel-item">
								<div class="img-box">
									<img src="images/oik1.png" alt="" />
								</div>
							</div>
							<div class="carousel-item">
								<div class="img-box">
									<img src="images/oik3.png" alt="" />
								</div>
							</div>
						</div>
						<div class="carousel_btn-container">
							<a
								class="carousel-control-prev"
								href="#carouselExampleControls"
								role="button"
								data-slide="prev"
							>
								<span class="carousel-control-prev-icon" aria-hidden="true" />
								<span class="sr-only">Previous</span>
							</a>
							<a
								class="carousel-control-next"
								href="#carouselExampleControls"
								role="button"
								data-slide="next"
							>
								<span class="carousel-control-next-icon" aria-hidden="true" />
								<span class="sr-only">Next</span>
							</a>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
	<!-- end slider section -->
</div>

<section class="product_section layout_padding">
	<div class="container">
		<div class="heading_container">
			<h2>Our Products</h2>
		</div>
		<div class="product_container">
			{#each perfumes as perfume}
				<div class="box">
					<div class="img-box">
						<img src={perfume.image} alt="" />
					</div>
					<div class="detail-box">
						<h5>{perfume.name}</h5>
						<h4>
							<span>$</span>{perfume.price}
						</h4>
						<a href="/"> Buy Now </a>
					</div>
				</div>
			{/each}
		</div>
		<div class="btn-box">
			<a href="/products"> See More </a>
		</div>
	</div>
</section>
<section class="product_section layout_padding">
	<div id="mapid" style="height: 500px;" />
</section>

<section class="blog_section layout_padding">
	<div class="container">
		<div class="heading_container">
			<h2>Our Blog</h2>
		</div>
		<div class="row">
			<div class="col-md-6">
				<div class="box">
					<div class="img-box">
						<img src="images/b-1.jpg" alt="" />
					</div>
					<div class="detail-box">
						<h3>New OIK Products</h3>
						<p>
							It is a long established fact that a reader will be distracted by the readable content
							of a page when looking at its layout. The point of using Lorem
						</p>
					</div>
				</div>
			</div>
			<div class="col-md-6">
				<div class="box">
					<div class="img-box">
						<img src="images/b-2.jpg" alt="" />
					</div>
					<div class="detail-box">
						<h3>New OIK Products</h3>
						<p>
							It is a long established fact that a reader will be distracted by the readable content
							of a page when looking at its layout. The point of using Lorem
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<Footer />

<style>
	.logo {
		height: 100px;
	}
	.popup-image {
		width: 10px;
	}
</style>
