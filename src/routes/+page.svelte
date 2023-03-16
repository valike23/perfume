<script lang="ts">
	import Header from '$lib/Header.svelte';
	import { onMount } from 'svelte';
	import Footer from '$lib/Footer.svelte';
	import Loading from '$lib/loading.svelte';
	import axios from 'axios';
	import { APPLICATION_URL } from '$lib/properties/init';
	import type { Iproduct } from '$lib/properties/model';
	let win: any = {};
  let loading = true;
  let perfumes :Iproduct[] = [];

	onMount(async () => {
		win = window;
    try {
    const data = await  axios.get(APPLICATION_URL + 'products/top_3');
    if(data){ 
      perfumes = data.data;
      loading = false;
    }
    } catch (error) {
      loading = false;
      perfumes = [];
    }
	});
</script>

{#if loading}
   <Loading/>
{:else}
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
        <img src="{perfume.image}" alt="" />
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
{/if}

<style>
	.logo {
		height: 100px;
	}
</style>
