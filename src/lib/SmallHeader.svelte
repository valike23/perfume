<script lang="ts">
	import { onMount } from 'svelte';
	import Nav from './Nav.svelte';

	let win: any = {};

	onMount(() => {
		win = window;
	});
	function openNav() {
		win.document.getElementById('myNav').classList.toggle('menu_width');
		win.document.querySelector('.custom_menu-btn').classList.toggle('menu_btn-style');
	}
</script>

<div class="hero_area ">
	<!-- header section strats -->
	<header class="header_section">
		<div class="container-fluid">
			<nav class="navbar navbar-expand-lg custom_nav-container">
				<a class="navbar-brand" href="index.html">
					<span> OIK </span>
				</a>
				<div class="" id="">
					<div class="User_option">
						<form class="form-inline my-2  mb-3 mb-lg-0">
							<input type="search" placeholder="Search" />
							<button class="btn   my-sm-0 nav_search-btn" type="submit" />
						</form>
						<a href="">
							<img src="images/bag.png" alt="" />
						</a>
					</div>

					<div class="custom_menu-btn">
						<button>
							<span class="s-1" />
							<span class="s-2" />
							<span class="s-3" />
						</button>
					</div>
					<Nav/>
				</div>
			</nav>
		</div>
	</header>
	<!-- end header section -->
</div>
