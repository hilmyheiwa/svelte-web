<script>
    import { onMount, onDestroy } from 'svelte';
    import  feather  from 'feather-icons';
  
    let showTopButton = false;
  
    onMount(() => {
      window.addEventListener('scroll', handleScroll);
      feather.replace()
    });
  
    onDestroy(() => {
      window.removeEventListener('scroll', handleScroll);
    });
  
    function scrollToTop() {
      window.scrollTo({ top: 0, behavior: "smooth" })
    }
  
    function handleScroll() {
      if (document.body.scrollTop >= 400 || document.documentElement.scrollTop >= 400) {
        showTopButton = true;
      } else {
        showTopButton = false;
      }
    }
  </script>
  
  <main>
    <!-- Back to top -->
    <!-- {#if showTopButton} -->
    <a href="#name" style={showTopButton ? '' : 'display: none'}  on:click={scrollToTop} id="back-to-top" class="back-to-top rounded fs-5">
      <i data-feather="arrow-up" class="fea icon-sm align-middle"></i>
    </a>
    <!-- {/if} -->
    <!-- Back to top -->
  </main>
  
  <style lang="scss">
    /* your styles here */
  </style>