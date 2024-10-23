<script lang="ts">
  // Keep existing tech stack
  const techStack = [
    { name: 'ReactJS', icon: '/icons/reactjs.svg' },
    { name: 'NextJS', icon: '/icons/nextjs.svg' },
    { name: 'VueJS', icon: '/icons/vuejs.svg' },
    { name: 'Javascript', icon: '/icons/javascript.svg' },
    { name: 'Golang', icon: '/icons/golang.svg' },
    { name: 'Python', icon: '/icons/python.svg' },
    { name: 'Django', icon: '/icons/django.svg' },
    { name: 'Java', icon: '/icons/java.svg' },
    { name: 'SpringBoot', icon: '/icons/springboot.svg' }
  ];

  // Add detailed experiences
  interface Experience {
    role: string;
    company: string;
    companyDescription?: string;
    period: string;
    location: string;
    workType: string;
    responsibilities: string[];
    skills: string[];
  }

  const experiences: Experience[] = [
    {
      role: "Junior Software Engineer",
      company: "Skor Technologies",
      period: "Sep 2024 - Present", 
      location: "Jakarta, Indonesia",
      workType: "Hybrid",
      responsibilities: [
        "Making the statement service and worker to scrape email, process pdf and extract the bill statement and credit card statement.",
        "Working with Golang for backend development.",
      ],
      skills: ["Golang", "Backend Development"]
    },
    {
      role: "Software Engineer Intern",
      company: "DOKU, PT NUSA SATU INTI ARTHA",
      companyDescription: "DOKU is a Grade 1 Payment Service Provider (PJP-1) in Indonesia founded in 2007, serving over 150K merchants and processing over 1B transactions.",
      period: "Mar 2024 - Sep 2024 · 7 mos",
      location: "Jakarta, Indonesia",
      workType: "Hybrid",
      responsibilities: [
        "Enhancing user B2B experience by building PHP SDK for merchant Doku Virtual Account, Token, and Direct Debit with a team of 4+.",
        "Testing the SDK in company's private VPS and in dev environment.",
        "Took a part in designing flow of the SDK Check Virtual Account."
      ],
      skills: ["PHP", "Agile Methodologies"]
    },
    {
      role: "Front End Intern",
      company: "Collega Inti Pratama, PT",
      period: "Jul 2023 - Oct 2023 · 4 mos",
      location: "Jakarta Selatan, Jakarta, Indonesia",
      workType: "On-site",
      responsibilities: [
        "Developing FrontEnd of SmartBranch BackEnd application for a bank in Indonesia as the client of Collega."
      ],
      skills: [
        "Cascading Style Sheets (CSS)",
        "Agile & Waterfall Methodologies",
        "Axios",
        "DaisyUI",
        "Git",
        "Scrum",
        "HTML5",
        "Tailwind CSS",
        "React.js",
        "REST APIs",
        "MaterialUI"
      ]
    }
  ];
</script>

<section class="w-full md:w-1/2 pr-8">
  <h2 class="text-2xl font-semibold mb-6 dark:text-white">Tech Stack</h2>
  <div class="grid grid-cols-3 gap-4 mb-12">
    {#each techStack as tech}
      <div class="flex items-center gap-2 p-2 bg-gray-100 dark:bg-gray-800 rounded-lg">
        <img src={tech.icon} alt={tech.name} class="w-6 h-6" />
        <span class="text-sm dark:text-gray-100">{tech.name}</span>
      </div>
    {/each}
  </div>

  <h2 class="text-2xl font-semibold mb-6 dark:text-white">Notable Experiences in Tech Industry</h2>
  {#each experiences as exp}
    <div class="mb-8 p-4 rounded-lg bg-gray-50 dark:bg-gray-800/50">
      <h3 class="text-xl font-medium mb-1 dark:text-white">{exp.role}</h3>
      <p class="text-gray-700 dark:text-gray-300 font-medium mb-1">{exp.company} · Internship</p>
      <p class="text-gray-600 dark:text-gray-400 mb-1">{exp.period}</p>
      <p class="text-gray-600 dark:text-gray-400 mb-2">{exp.location} · {exp.workType}</p>
      
      {#if exp.companyDescription}
        <p class="text-gray-700 dark:text-gray-300 mb-3">{exp.companyDescription}</p>
      {/if}

      <ul class="list-disc list-inside mb-3 space-y-1">
        {#each exp.responsibilities as responsibility}
          <li class="text-gray-700 dark:text-gray-300">{responsibility}</li>
        {/each}
      </ul>

      <div class="mt-3">
        <span class="font-medium dark:text-white">Skills: </span>
        <span class="text-gray-700 dark:text-gray-300">{exp.skills.join(' · ')}</span>
      </div>
    </div>
  {/each}
</section>