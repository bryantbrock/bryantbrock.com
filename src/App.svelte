<script>
  import DevOps from 'pages/DevOps.svelte';
  import FullStackApps from 'pages/FullStackApps.svelte';
  import ScriptsAndApis from 'pages/ScriptsAndApis.svelte';
  import Portfolio from 'pages/Portfolio.svelte';
  import Footer from 'partials/Footer.svelte';
  import Sidebar from 'partials/Sidebar.svelte';
  import Tailwind from 'partials/Tailwind.svelte';
  import {getUrlParams} from 'util/misc.js';

  const pages = [
    {page: 'dev-ops', Component: DevOps},
    {page: 'full-stack-apps', Component: FullStackApps},
    {page: 'scripts-and-apis', Component: ScriptsAndApis},
  ];

  const params = getUrlParams();
  const pageExists = pages.map(val => val.page).includes(params.page);
  const isHome = window.location.pathname.length < 2 && !window.location.search

  // Redirect to home on 404
  if ((params.page && !pageExists) || window.location.pathname.length > 1) {
    window.location.href = window.location.origin;
  }
</script>

<Tailwind />

<div class="bg-gray-50 min-h-screen base">

  <!-- Static views -->
  <div class="max-w-screen-lg mx-auto">
    <div class="flex">
      <Sidebar />
      {#if isHome}
        <Portfolio />
      {/if}
      {#each pages as {page, Component}}
        {#if page === params.page}
          <Component />
        {/if}
      {/each}
    </div>
    <Footer />
  </div>

</div>