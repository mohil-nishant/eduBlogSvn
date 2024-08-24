<script>
    import { fly } from 'svelte/transition';
    import { quintOut } from 'svelte/easing';
    import logo from '$lib/assets/logo.png';
  
    let logoName = 'SVN NAHAN';
    let isMenuOpen = false;
  
    function toggleMenu() {
      isMenuOpen = !isMenuOpen;
    }
  
    const navigationLinks = [
      { name: 'Fee info', url: '/fee' },
      { name: 'student', url: '/students' },
      { name: 'Results', url: '/results' },
      { name: 'Courses', url: '/courses' },
      { name: 'Projects', url: '/projects' },
      { name: 'Mandatory Disclosure', url: '/disclosure' }
    ];
  </script>
  
  <header class="static top-0 bg-indigo-50">
    <div class="mx-auto flex h-16 max-w-screen-xl items-center gap-8 px-4 sm:px-6 lg:px-8">
      <a class="text-svnblue flex items-center justify-center gap-2" href="/">
        <span class="sr-only">Home</span>
        <img src={logo} alt="logo" class="w-14" />
        <p class="sm:hidden font-extrabold text-lg text-svnblue">{logoName}</p>
      </a>
  
      <div class="flex flex-1 items-center justify-end md:justify-between">
        <nav aria-label="Global" class="hidden md:block">
          <ul class="flex items-center gap-6 text-sm">
            {#each navigationLinks as link}
              <li>
                <a class="text-svnblue transition hover:text-svnblue font-semibold" href={link.url}>
                  {link.name}
                </a>
              </li>
            {/each}
          </ul>
        </nav>
        <div class="flex items-center gap-4">
          <button
            class="block rounded p-2.5 text-svnblue transition hover:text-gray-600/75 md:hidden"
            on:click={toggleMenu}
          >
            <span class="sr-only">Toggle menu</span>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="size-8 text-svnblue"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              {#if !isMenuOpen}
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M3.75 6.75h16.5M3.75 12h16.5M12 17.25h8.25"
                />
              {:else}
                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
              {/if}
            </svg>
          </button>
        </div>
      </div>
    </div>
  </header>
  
  {#if isMenuOpen}
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div class="fixed inset-0 bg-black bg-opacity-50 z-40" on:click={toggleMenu}></div>
    <div
      class="fixed top-0 right-0 w-64 h-full bg-white shadow-lg z-50"
      transition:fly={{ x: 300, duration: 300, easing: quintOut }}
    >
      <div class="p-4">
        <div class="flex items-center justify-between">
          <h2 class="text-xl font-bold mb-4 text-svnblue">Menu</h2>
          <button
            class="block rounded p-2.5 text-svnblue transition hover:text-gray-600/75 md:hidden"
            on:click={toggleMenu}
          >
            <span class="sr-only">Toggle menu</span>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="size-8 text-svnblue"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
  
        <ul class="space-y-3">
          {#each navigationLinks as link}
            <li>
              <a
                href={link.url}
                on:click={toggleMenu}
                class="block rounded-lg bg-indigo-100 px-4 py-2 text-sm font-medium text-gray-700 hover:bg-indigo-200 transition-colors"
              >
                {link.name}
              </a>
            </li>
          {/each}
        </ul>
      </div>
    </div>
  {/if}
  