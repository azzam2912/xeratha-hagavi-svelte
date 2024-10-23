<script lang="ts">
  interface TeachingExperience {
    role: string;
    organization: string;
    type: string;
    period: string;
    location: string;
    workType: string;
    description?: string;
  }

  const teachingExperiences: TeachingExperience[] = [
    {
      role: "Math Olympiad Tutor",
      organization: "Star Generation",
      type: "Part-time",
      period: "Apr 2024 - Present · 7 mos",
      location: "Jakarta",
      workType: "Remote",
      description: "Taught math olympiad for private students, group classes and intensive camps for grade 3-8. Using English as the main language."
    },
    {
      role: "Tutoring Universitas Indonesia Contingent for ONMIPA Matematika 2024",
      organization: "Universitas Indonesia",
      type: "Part-time",
      period: "March 2024 - April 2024",
      location: "Jakarta",
      workType: "Hybrid"
    },
    {
      role: "Tutoring SMAN 8 Jakarta for OSK Matematika 2024",
      organization: "SMAN 8 Jakarta",
      type: "Part-time",
      period: "January 2024 - March 2024",
      location: "Jakarta",
      workType: "On-site"
    },
    {
      role: "Private Tutoring a student from Jawa Timur for OSN SMA Matematika 2023",
      organization: "Private",
      type: "Part-time",
      period: "May 2023 - June 2023",
      location: "Remote",
      workType: "Remote"
    }
  ];

  const achievements = [
    {
      title: "Gold Medal ONMIPA Matematika 2022 National Level",
      year: "2022"
    },
    {
      title: "Bronze Medal OSN Matematika 2019 National Level",
      year: "2019"
    },
    {
      title: "Finalist ICPC (International Collegiate Programming Contest) Asia Jakarta 2023",
      year: "2023"
    }
  ];
</script>

<section class="w-full md:w-1/2 pl-8 border-l border-gray-200 dark:border-gray-700">
  <h2 class="text-2xl font-semibold mb-6 dark:text-white">Notable Math Olympiad and Competitive Programming Achievement</h2>
  {#each achievements as achievement}
    <div class="mb-6">
      <h3 class="text-xl font-medium mb-2 dark:text-white">{achievement.title}</h3>
      <p class="text-gray-600 dark:text-gray-400">{achievement.year}</p>
    </div>
  {/each}

  <h2 class="text-2xl font-semibold mb-6 mt-12 dark:text-white">Notable Math Olympiad Tutoring Experiences</h2>
  {#each teachingExperiences as exp}
    <div class="mb-8 p-4 rounded-lg bg-gray-50 dark:bg-gray-800/50">
      <h3 class="text-xl font-medium mb-1 dark:text-white">{exp.role}</h3>
      <p class="text-gray-700 dark:text-gray-300 font-medium mb-1">{exp.organization} · {exp.type}</p>
      <p class="text-gray-600 dark:text-gray-400 mb-1">{exp.period}</p>
      <p class="text-gray-600 dark:text-gray-400 mb-2">{exp.location} · {exp.workType}</p>
      
      {#if exp.description}
        <p class="text-gray-700 dark:text-gray-300">{exp.description}</p>
      {/if}
    </div>
  {/each}
</section>