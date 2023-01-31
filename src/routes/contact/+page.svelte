<script lang="ts">
	import { onMount } from "svelte";
	import Footer from "$lib/Footer.svelte";
    import Header from "$lib/Header.svelte";
	import SmallHeader from "$lib/SmallHeader.svelte";
	import Bottom from "$lib/Bottom.svelte";
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
  <Header></Header>


</div>

<section class="contact_section layout_padding" style="margin-top: -100px">
    <div class="container ">
      <h2 class="">
        Request A Call Back
      </h2>
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
              <button>
                SEND
              </button>
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
            <h2>
              Newsletter
            </h2>
          </div>
          <div class="col-md-8 col-lg-9">
            <form action="">
              <input type="text" placeholder="Enter your email">
              <button>
                Subscribe
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>

  <Footer></Footer>
  <Bottom></Bottom>