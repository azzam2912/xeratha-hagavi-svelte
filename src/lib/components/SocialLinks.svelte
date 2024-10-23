<script lang="ts">
  const socialLinks = [
    {
      name: 'Instagram Personal',
      icon: '/icons/instagram.svg',
      url: 'https://www.instagram.com/azzam_29_12'
    },
    {
      name: 'Instagram Math Account',
      icon: '/icons/instagram.svg',
      url: 'https://www.instagram.com/haxuv.world'
    },
    {
      name: 'LinkedIn',
      icon: '/icons/linkedin.svg',
      url: 'https://www.linkedin.com/in/azzam-labib-hakim-b8212b1a3/'
    },
    {
      name: 'Twitter / X',
      icon: '/icons/xtwitter.svg',
      url: 'https://twitter.com/xeratha_haxuv/'
    },
    {
      name: 'Github',
      icon: '/icons/github.svg',
      url: 'https://github.com/azzam2912'
    }
  ];
</script>

<section class="mb-12">
  <h2 class="text-2xl font-semibold mb-6 dark:text-white">Let's connect and work together!</h2>
  <div class="flex flex-wrap gap-4">
    {#each socialLinks as link}
      <a
        href={link.url}
        class="flex items-center gap-2 px-4 py-2 bg-gray-800 dark:bg-gray-700 hover:bg-gray-700 dark:hover:bg-gray-600 text-white rounded-lg transition-all duration-300"
        target="_blank"
        rel="noopener noreferrer"
      >
        <img src={link.icon} alt="" class="w-5 h-5" />
        <span>{link.name}</span>
      </a>
    {/each}
  </div>
</section>