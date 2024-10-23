<script lang="ts">
  import Header from '$lib/components/Header.svelte';
  import Skills from '$lib/components/Skills.svelte';
  import Teaching from '$lib/components/Teaching.svelte';
  import SocialLinks from '$lib/components/SocialLinks.svelte';
  import ThemeToggle from '$lib/components/ThemeToggle.svelte';
</script>

<div class="min-h-screen bg-white dark:bg-gray-900 text-gray-900 dark:text-gray-100 transition-colors duration-300">
  <ThemeToggle />
  <main class="max-w-6xl mx-auto px-4 py-8">
    <Header />
    <SocialLinks />
    <div class="flex flex-col md:flex-row gap-8">
      <Skills />
      <Teaching />
    </div>
  </main>
</div>