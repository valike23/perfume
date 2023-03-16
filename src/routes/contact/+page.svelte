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

<section class="contact_section layout_padding" style="margin-top: -100px">
	<div class="container ">
		<h2 class="">Request A Call Back</h2>
	</div>
	<div class="container">
		<div class="row">
			<div class="col-md-8 col-lg-6 mx-auto">
				<form action="">
					<div>
						<input type="text" placeholder="Name" />
					</div>
					<div>
						<input type="email" placeholder="Email" />
					</div>
					<div>
						<input type="text" placeholder="Phone Number" />
					</div>
					<div>
						<input type="text" class="message-box" placeholder="Message" />
					</div>
					<div class="d-flex justify-content-center">
						<button> SEND </button>
					</div>
				</form>
			</div>
		</div>
	</div>
</section>

<section class="subscribe_section mt-3">
	<div class="container">
		<div class="box">
			<div class="row">
				<div class="col-md-4 col-lg-3">
					<h2>Newsletter</h2>
				</div>
				<div class="col-md-8 col-lg-9">
					<form action="">
						<input type="text" placeholder="Enter your email" />
						<button> Subscribe </button>
					</form>
				</div>
			</div>
		</div>
	</div>
</section>

<Footer />
<Bottom />
