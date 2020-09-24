<script>
  import Header from "./components/Header.svelte";
  import Sidebar from "./components/Sidebar.svelte";

  import Footer from "./components/Footer.svelte";

  let showHeader = false;
  let showFooter = false;

  function onKeyDown(e) {
    switch (e.keyCode) {
      case 70:
        showFooter = !showFooter;
        break;
      case 72:
        showHeader = !showHeader;
        break;
    }
  }
</script>

<style>
</style>

<div class="wrapper">
  <Header visible={showHeader} />

  <div class="middle">
    <div class="container">
      <main class="content" />
      <!-- .content -->
    </div>
    <!-- .container-->
    <Sidebar />
    <!-- .right-sidebar -->
  </div>
  <!-- .middle-->
</div>
<!-- .wrapper -->

<Footer visible={showFooter} />
<svelte:window on:keydown|preventDefault={onKeyDown} />
