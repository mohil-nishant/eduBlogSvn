<script>
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';
	import '../app.css';
</script>
<div>
  <!-- sticky header -->
  <header class="sticky top-0 ..."><Header /></header>
  <!-- end sticky header -->

  <div class="">
    <p class=""><slot /></p>
  </div>
</div>
<Footer />
<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.100);
	}
</style>
