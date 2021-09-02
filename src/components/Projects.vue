<template>
  <div id="projects">
    <p
      class="text-md md:text-xl font-semibold"
      style="letter-spacing: -0.05 rem;"
    >
      Here's a list of things I've done recently
    </p>
    <div class="text-sm md:text-lg">
      <ul v-for="p in projects" class="mx-6 my-3 md:my-4 list-disc">
        <li class="space-y-1">
          <a class="font-medium" :href="p.link">
            {{ p.name }}
          </a>
          <div class="block space-y-1.5">
            <span
              class="block font-light text-xs"
              v-for="n in p.notes"
            >
              {{ n }}
            </span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Projects',
  setup: () => {
    const projects = [
      {
        name: 'Yamanote Line Station Information Screen',
        link: 'https://wonderful-bohr-b3db75.netlify.app',
        notes: [
          'Replicated Tokyo’s Yamanote Line’s station information screen for web using SVG for graphics'
        ]
      },
      {
        name: 'Better Yahoo Transit JP',
        link: 'https://secure-earth-69090.herokuapp.com',
        notes: [
          'Created Python API library for Yahoo Japan’s private Transit API',
          'Better, Google-like front-end for Japan Yahoo Transit using Mapbox for maps'
        ]
      },
      {
        name: 'Spotify Playback Speed UI Extension',
        link: 'https://github.com/rnikko/spotify-playback-speed',
        notes: [
          'UI Extension to quickly change playback speed setting on Spotify Web'
        ]
      },
      {
        name: 'Weathernews Python API Library',
        link: 'https://github.com/rnikko/weathernews-python',
        notes: [
          'Library which provides convenient access to data provided by weather website Weathernews.jp'
        ]
      },
      {
        name: 'General Purpose + Music Discord Bot',
        link: 'https://github.com/rnikko/sportjoke-dev',
        notes: [
          'Discord chat bot which provides similar features to paid bots, but for free',
          'Hosting and present in 15+ servers, across 3000+ users'
        ]
      }
    ]

    // ping heroku apps so they aren't idle
    for (const p of projects) {
      if (p.link.indexOf('herokuapp') >= 0) {
        fetch(p.link)
      }
    }
    return {
      projects
    }
  }
}
</script>
