<script lang="ts">
	import Header from "$lib/Header.svelte";
import { onMount } from "svelte";
	import Footer from "$lib/Footer.svelte";
let win:any = {};

onMount(()=>{
  win = window;
 
})




</script>

<div class="hero_area pt-5 ">
  <!-- header section strats -->
<Header></Header>
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
          <img src="images/products/blue_de_channel.jpg" alt="">
        </div>
        <div class="detail-box">
          <h5>
          Blue De Channel
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
          <img src="images/products/channel_chance.jpg" alt="">
        </div>
        <div class="detail-box">
          <h5>
          Channel Chance
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
          <img src="images/products/Dior_home.jpg" alt="">
        </div>
        <div class="detail-box">
          <h5>
         Dior Home
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






<style>
  .logo{
    height: 100px;
  }
</style>