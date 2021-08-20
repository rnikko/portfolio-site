<template>
  <div id="projects" class="text-md md:text-xl font-semibold">
    <p style="letter-spacing: -0.05 rem;">
      Here's a list of things I've done recently
    </p>
    <div class="text-sm md:text-xl font-light">
      <ul v-for="p in projects" class="mx-6 my-3 md:my-4 list-disc">
        <li>
          <a :href="p.link">
            {{ p.name }}
          </a>
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
        'name': 'Weathernews Python API Library',
        'link': 'https://github.com/rnikko/weathernews-python'
      },
      {
        'name': 'Yamanote Line Station Information Screen',
        'link': ''
      },
      {
        'name': 'Better Yahoo Transit JP',
        'link': ''
      },
      {
        'name': 'General Purpose + Music Discord Bot',
        'link': 'https://github.com/rnikko/sportjoke-dev'
      },
      {
        'name': 'Spotify Playback Speed Chrome Extension',
        'link': 'https://github.com/rnikko/spotify-playback-speed'
      }
    ]
    return {
      projects
    }
  }
}
</script>
