<script>
  const projects = [
    {
      type: 'mock',
      link: 'https://www.linkedin.com/feed/update/urn:li:activity:6909269606574559233/',
      title: 'PayPal Mobile App',
      company: 'Freelance',
      start: 'MAR 2022',
      end: 'PRESENT',
      description: `
        I created a mock PayPal application to showcase how quickly I was able to build a mobile
        application using a React Native. I'm highly experienced with React and was able to pick
        up React Native for mobile development very quickly. This mock took 6 hours; UX and navigation
        but no functionality (e.g. processing payments, naturally) was included.
      `
    },
  ];

  const techStackRows = ['Client', 'Middleware', 'Database', 'Deployment'];
  const techStacks = [
    ['React Native', 'Node.js', 'DynamoDB', 'Heroku / Serverless / AWS'],
    ['React Native', 'Flask (Python)', 'PostgreSQL', 'Heroku / AWS'],
  ];
</script>

<div class="p-6">
  <div>
    <a href="/" class="font-bold">{'< '} <span class="ml-1">Home</span></a>
  </div>
  <div class="mt-8">
    <h1 class="text-3xl font-bold">Mobile Applications</h1>
    <hr class="my-3 w-full" />
    <p>
      Mobile applications are really a subset of
      <a href='/?page=full-stack-apps' class="text-blue-800 hover:text-blue-900 underline">
        Full Stack Applications
      </a>.

      The main difference is that mobile apps don't run on the web; they run specifically
      for IOS or Android. That being said, once you have created your UX in React Native (my choice),
      you can easily hook it up to existing APIs to handle all the logic for your application.
      <br />
      <br />
      With heavy experience in the
      <a href='/?page=full-stack-apps' class="text-blue-800 hover:text-blue-900 underline">
        Full Stack Applications
      </a> world, mobile apps have been an easy pickup along the way. They integrate easily
      with many APIs I've built, and with React Native, my JavaScript skills have ported over excellently.
    </p>
  </div>
  <div class="mt-10">
    <h2 class="tracking-wide text-xl">PROJECTS</h2>
    {#each projects as {type, link, title, company, start, end, description}}
      <div class="my-4">
        <div>
          <a href={link} class="text-blue-800 hover:text-blue-900 underline" target="_blank">
            <span class="text-xs">[{type}]</span>
            <span>{title}</span>
          </a>
          <span> - </span>
          <span class="italic">{company}</span>
        </div>
        <span class="text-gray-600 text-sm">{start} - {end}</span>
        <p>{description}</p>
      </div>
    {/each}
  </div>
  <div class="mt-10">
    <h2 class="tracking-wide text-xl">TECH STACKS</h2>
    <div class="flex">
      <div class="flex flex-col mt-6">
        {#each techStackRows as row}
          <span class="text-gray-400 align-middle text-right my-1">{row}</span>
        {/each}
      </div>
      {#each techStacks as stack}
        <div class="flex flex-col mt-6 ml-4 border-l pl-4">
          {#each stack as level}
            <span class="align-middle my-1">{level}</span>
          {/each}
        </div>
      {/each}
    </div>
  </div>
</div>
