<script lang="ts">
  import Header from './header.svelte';
  import Footer from './footer.svelte';

  import '../app.css';
  import 'sanitize.css';
</script>

<div class="layout">
  <Header />

  <main>
    <slot />
  </main>

  <Footer />
</div>
