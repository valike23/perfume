<script>
	import Bottom from '$lib/Bottom.svelte';
	import Footer from '$lib/Footer.svelte';
	import Header from '$lib/Header.svelte';
</script>

<div class="hero_area pt-5 ">
	<Header />
</div>
<div class="container my-5">
    <div class="row">
      <div class="col-md-6">
        <img src="https://via.placeholder.com/500x500" alt="Product Image" class="img-fluid">
      </div>
      <div class="col-md-6">
        <h1 class="fw-bold">Product Name</h1>
        <p class="lead my-4">$50</p>
        <p class="mb-4">Product description goes here. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eu mi lorem. Pellentesque at ipsum vel lorem lacinia fringilla euismod et justo.</p>
        <form>
          <div class="mb-3">
            <label for="quantity" class="form-label">Quantity:</label>
            <input type="number" id="quantity" class="form-control" value="1">
          </div>
          <button type="submit" class="btn btn-primary">Add to Cart</button>
        </form>
      </div>
    </div>
  </div>
<Footer />
<Bottom />
