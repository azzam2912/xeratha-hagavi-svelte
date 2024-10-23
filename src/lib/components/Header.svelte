<script lang="ts">
  const name: string = "fmt.Println(\"Azzam\")";
  const title: string = "Software Engineer & Math Olympiad Teacher";
</script>

<header class="text-center mb-16">
  <!-- Add profile photo -->
  <div class="mb-6 flex justify-center">
    <img
      src="/self-portrait.jpeg" 
      alt="Profile"
      class="w-32 h-32 rounded-full border-4 border-gray-200 dark:border-gray-700 shadow-lg"
    />
  </div>
  
  <h1 class="text-2xl md:text-4xl font-bold mb-2 font-mono dark:text-white">{name}</h1>
  <p class="text-xl text-gray-600 dark:text-gray-400">{title}</p>
</header>