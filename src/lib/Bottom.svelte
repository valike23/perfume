<script lang="ts">
	import { onMount } from "svelte";



let win:any = {};

onMount(()=>{
  win = window;
  getYear();
})
function getYear() {
    var currentDate = new Date();
    var currentYear = currentDate.getFullYear();
    win.document.querySelector("#displayYear").innerHTML = currentYear;
}
</script>



<section class="container-fluid footer_section ">
    <div class="container">
      <p>
        &copy; <span id="displayYear"></span> All Rights Reserved. Design by
        <a href="https://valentine-emmanuel-ikechukwu.com">Valentine Emmanuel Ikechukwu</a>
      </p>
    </div>
  </section>