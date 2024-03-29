<script>
  import Card from 'partials/Card.svelte';

  const scriptsAndApis = {
    title: 'One-off Scripts & APIs',
    path: '/?page=scripts-and-apis',
    body:
      `I can build any API or one-off script that gathers
      data from third-parties, web scraping, and much more.
      Again, if you can dream it, I can build it.`
  };

  const fullStackApps = {
    title: 'Full Stack Applications',
    path: '/?page=full-stack-apps',
    body:
      `4+ yrs of experience developing startup and large-scale
      web applications. If you can dream it, I can build it.`
  };

  const devOps = {
    title: 'Dev Ops',
    path: '/?page=dev-ops',
    body:
      `Experienced configuring and deploying web applications and
      APIs to AWS.`
  };

  const mobileApps = {
    title: 'Mobile Applications',
    path: '/?page=mobile-apps',
    body:
      `Experienced using React Native to build mobile applications.`
  };
</script>

<div class="p-6">
  <h1 class="text-3xl font-bold mr-16">Full Stack Software Engineer</h1>
  <div class="flex mt-4">
    <div class="flex">
      <a
        target="_blank"
        rel="noreferrer"
        href="https://github.com/bryantbrock"
        class="rounded-full mr-2 max-w-sm">
        <img
          class="rounded-full w-8 opacity-60 hover:opacity-80 transition"
          alt="Github"
          src="assets/github.png" />
      </a>
      <a
        target="_blank"
        rel="noreferrer"
        href="https://www.linkedin.com/in/bryantleebrock"
        class="rounded-full mr-2">
        <img
          class="rounded-full w-8 opacity-60 hover:opacity-80 transition"
          alt="LinkedIn"
          src="assets/linkedin.png" />
      </a>
    </div>
    <div class="flex flex-wrap">
      <a
        target="_blank"
        rel="noreferrer"
        href="/assets/2023-resume.pdf"
        class="py-1 mb-1 px-6 ml-4 border border-black rounded hover:bg-gray-100 transition">
        Resume
      </a>
      <a
        target="_blank"
        rel="noreferrer"
        href="https://medium.com/@bryantbrock"
        class="py-1 px-6 mb-1 ml-4 border border-black rounded hover:bg-gray-100 transition">
        Blog
      </a>
    </div>
  </div>
  <div class="mt-10">
    <div class="grid grid-cols-2 gap-2">
      <Card {...fullStackApps} />
      <Card {...devOps} />
      <Card {...scriptsAndApis} />
      <Card {...mobileApps} />
    </div>
  </div>
  <div class="mt-12">
    <h2 class="text-xl font-bold">Methodology</h2>
    <p class="mt-6">
      Software engineering isn’t about the languages you know, the frameworks you have used,
      nor the code you can write. A good software engineer is someone who can learn any language,
      any framework, any cloud service at a rapid pace. To put it another way, a skilled
      software engineer is one who not only learns, but is good at learning.
      <br /><br />

      What sets me apart? I know how to read and implement <strong>documentation</strong>.
      The documentation can teach you everything you need to know; from there, it’s just manual labor.
      <br /><br />

      I stick to two primary languages: <strong>JavaScript (TypeScript)</strong> and <strong>Python</strong>.
      These two languages have matured over tha past two decades to accomplish 99% of any
      software project, whether it be a SaaS application, a REST API, or a one-off Python/Node script.
      <br /><br />
    </p>
  </div>
</div>
