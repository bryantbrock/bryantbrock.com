<script>
  const skills = [
    {name: 'React.js', pct: '100'},
    {name: 'Python', pct: '95'},
    {name: 'Node.js / Express.js', pct: '85'},
    {name: 'AWS S3 / EC2 / RDS / Lambda', pct: '80'},
    {name: 'Serverless Framework', pct: '65'},
    {name: 'Heroku', pct: '90'},
    {name: 'Docker', pct: '60'},
    {name: 'Django / Flask / Werkzeug', pct: '55'},
  ];
</script>

<div id="sidebar" class="ml-6 my-6 pr-6 mr-6 border-r border-gray-400">
  <img src="assets/headshot.jpg" alt="headshot" class="rounded h-64" />
  <div class="mt-6">
    <h2 class="font-bold text-xl">Bryant Brock</h2>
    <span class="text-gray-500 -mt-1">
      Software Engineer
    </span>
  </div>
  <div class="mt-6">
    <p>Moscow, ID</p>
    <p>(770) 820-8961</p>
    <p>bryanteebrock@gmail.com</p>
  </div>
  <div class="mt-6">
    <h3 class="mb-1 font-bold text-lg">Education & Experience</h3>
    <ul>
      <li>B.A. from New Saint Andrews</li>
      <li>3+ years of experience</li>
    </ul>
  </div>
  <div class="mt-8">
    <h3 class="mb-1 font-bold text-lg">Top Skills</h3>
    <div>
      {#each skills as {name, pct}}
      <div class="flex flex-col mt-4 w-56">
        <span>{name}</span>
        <progress value={pct} max="100" class="w-full" />
      </div>
      {/each}
    </div>
  </div>
</div>

<style>
  progress {
    border-radius: 3px;
    height: 5px;
  }

  progress::-webkit-progress-bar {
    background-color: #33333333;
    border-radius: 3px;
  }

  progress::-webkit-progress-value {
    background-color: #333333;
    border-radius: 3px;
  }

  @media only screen and (max-width: 800px) {
    #sidebar {
      display: none;
    }
  }
</style>