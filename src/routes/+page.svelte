<script lang="ts">
	import { onMount } from "svelte";
	import Footer from "../lib/Footer.svelte";
let win:any = {};

onMount(()=>{
  win = window;
  getYear();
})
  function openNav() {
    win.document.getElementById("myNav").classList.toggle("menu_width")
    win.document.querySelector(".custom_menu-btn").classList.toggle("menu_btn-style")
}
function getYear() {
    var currentDate = new Date();
    var currentYear = currentDate.getFullYear();
    win.document.querySelector("#displayYear").innerHTML = currentYear;
}


</script>

<div class="hero_area pt-5 ">
  <!-- header section strats -->
  <header class="header_section">
    <div class="container-fluid">
      <nav class="navbar navbar-expand-lg custom_nav-container">
        <a class="navbar-brand" href="/">
          <span>
           <!-- svelte-ignore a11y-missing-attribute -->
           <img class="logo" src="logo.png" />
          </span>
        </a>
        <div class="" id="">
          <div class="User_option">
            <form class="form-inline my-2  mb-3 mb-lg-0">
              <input type="search" placeholder="Search">
              <button class="btn   my-sm-0 nav_search-btn" type="submit"></button>
            </form>
            <a href="/">
              <img src="images/bag.png" alt="">
            </a>
          </div>

          <div class="custom_menu-btn">
            <button on:click={openNav}>
              <span class="s-1">

              </span>
              <span class="s-2">

              </span>
              <span class="s-3">

              </span>
            </button>
          </div>
          <div id="myNav" class="overlay">
            <div class="overlay-content">
              <a href="/">Home</a>
              <a href="/">About</a>
              <a href="/">Products</a>
              <a href="/">Blog</a>
              <a href="/">Contact Us</a>
            </div>
          </div>
        </div>
      </nav>
    </div>
  </header>
  <!-- end header section -->
  <!-- slider section -->
  <section class="slider_section">
    <div class="side-img">
      <img src="images/side-img.png" alt="">
    </div>
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <div class="detail-box">
            <h2>
              Body Spray
            </h2>
            <h1>
              O<span>I</span>K
            </h1>
            <a href="/">
              Read More
            </a>
          </div>
        </div>
        <div class="col-md-6">
          <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
            <div class="carousel-inner">
              <div class="carousel-item active">
                <div class="img-box">
                  <img src="images/oik2.png" alt="">
                </div>
              </div>
              <div class="carousel-item">
                <div class="img-box">
                  <img src="images/oik1.png" alt="">
                </div>
              </div>
              <div class="carousel-item">
                <div class="img-box">
                  <img src="images/oik3.png" alt="">
                </div>
              </div>
            </div>
            <div class="carousel_btn-container">
              <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="sr-only">Previous</span>
              </a>
              <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
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
      <h2>
        Our Products
      </h2>
    </div>
    <div class="product_container">
      <div class="box">
        <div class="img-box">
          <img src="images/products/joanpaul.png" alt="">
        </div>
        <div class="detail-box">
          <h5>
            Joan Paul
          </h5>
          <h4>
            <span>$</span>100
          </h4>
          <a href="">
            Buy Now
          </a>
        </div>
      </div>
      <div class="box">
        <div class="img-box">
          <img src="images/products/greed_adventus.png" alt="">
        </div>
        <div class="detail-box">
          <h5>
          Greed Adventus
          </h5>
          <h4>
            <span>$</span>100
          </h4>
          <a href="">
            Buy Now
          </a>
        </div>
      </div>
      <div class="box">
        <div class="img-box">
          <img src="images/products/dior-sauvage.png" alt="">
        </div>
        <div class="detail-box">
          <h5>
           Dior Sauvage
          </h5>
          <h4>
            <span>$</span>100
          </h4>
          <a href="">
            Buy Now
          </a>
        </div>
      </div>
      <div class="box">
        <div class="img-box">
          <img src="images/products/cocochanel.png" alt="">
        </div>
        <div class="detail-box">
          <h5>
           Coco Chanel
          </h5>
          <h4>
            <span>$</span>100
          </h4>
          <a href="">
            Buy Now
          </a>
        </div>
      </div>
      <div class="box">
        <div class="img-box">
          <img src="images/products/baccarrouge.png" alt="">
        </div>
        <div class="detail-box">
          <h5>
            Baccar Rouge
          </h5>
          <h4>
            <span>$</span>100
          </h4>
          <a href="">
            Buy Now
          </a>
        </div>
      </div>
      <div class="box">
        <div class="img-box">
          <img src="images/products/blackorchid.png" alt="">
        </div>
        <div class="detail-box">
          <h5>
            Black Orchid
          </h5>
          <h4>
            <span>$</span>100
          </h4>
          <a href="">
            Buy Now
          </a>
        </div>
      </div>
    </div>
    <div class="btn-box">
      <a href="">
        See More
      </a>
    </div>
  </div>
</section>


<section class="blog_section layout_padding">
  <div class="container">
    <div class="heading_container">
      <h2>
        Our Blog
      </h2>
    </div>
    <div class="row">
      <div class="col-md-6">
        <div class="box">
          <div class="img-box">
            <img src="images/b-1.jpg" alt="">
          </div>
          <div class="detail-box">
            <h3>
              New OIK Products
            </h3>
            <p>
              It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <div class="box">
          <div class="img-box">
            <img src="images/b-2.jpg" alt="">
          </div>
          <div class="detail-box">
            <h3>
              New OIK Products
            </h3>
            <p>
              It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. The point of using Lorem
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<Footer></Footer>



<section class="container-fluid footer_section ">
  <div class="container">
    <p>
      &copy; <span id="displayYear"></span> All Rights Reserved. Design by
      <a href="https://valentine-emmanuel-ikechukwu.com">Valentine Emmanuel Ikechukwu</a>
    </p>
  </div>
</section>


<style>
  .logo{
    height: 100px;
  }
</style>