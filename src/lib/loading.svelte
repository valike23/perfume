  <!-- Create the loader element -->
  <div class="loader">
    <p>Loading...</p>
  </div>

<style>
    /* Set the styles for the loader */
    .loader {
      position: fixed;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: #fff;
      z-index: 9999;
      text-align: center;
    }
    
    /* Set the styles for the loading text */
    .loader p {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 24px;
      font-weight: bold;
    }
</style>