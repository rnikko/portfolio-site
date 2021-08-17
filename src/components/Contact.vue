<template>
  <div id="contact">
    <!-- <p class="text-md md:text-xl font-semibold my-3 md:my-4" style="letter-spacing: -0.05 rem;">
      Contact
    </p> -->
    <div class="space-x-6">
      <div class="space-x-2 inline-flex">
        <svg width="24" height="24" fill="currentColor">
          <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.463 2 11.97c0 4.404 2.865 8.14 6.839 9.458.5.092.682-.216.682-.48 0-.236-.008-.864-.013-1.695-2.782.602-3.369-1.337-3.369-1.337-.454-1.151-1.11-1.458-1.11-1.458-.908-.618.069-.606.069-.606 1.003.07 1.531 1.027 1.531 1.027.892 1.524 2.341 1.084 2.91.828.092-.643.35-1.083.636-1.332-2.22-.251-4.555-1.107-4.555-4.927 0-1.088.39-1.979 1.029-2.675-.103-.252-.446-1.266.098-2.638 0 0 .84-.268 2.75 1.022A9.606 9.606 0 0112 6.82c.85.004 1.705.114 2.504.336 1.909-1.29 2.747-1.022 2.747-1.022.546 1.372.202 2.386.1 2.638.64.696 1.028 1.587 1.028 2.675 0 3.83-2.339 4.673-4.566 4.92.359.307.678.915.678 1.846 0 1.332-.012 2.407-.012 2.734 0 .267.18.577.688.48C19.137 20.107 22 16.373 22 11.969 22 6.463 17.522 2 12 2z">
          </path>
        </svg>
        <span><a :href="github">Github</a></span>
      </div>
      <div class="space-x-2 inline-flex">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" style="padding: 2px" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M2.94 6.412A2 2 0 002 8.108V16a2 2 0 002 2h12a2 2 0 002-2V8.108a2 2 0 00-.94-1.696l-6-3.75a2 2 0 00-2.12 0l-6 3.75zm2.615 2.423a1 1 0 10-1.11 1.664l5 3.333a1 1 0 001.11 0l5-3.333a1 1 0 00-1.11-1.664L10 11.798 5.555 8.835z" clip-rule="evenodd" />
        </svg>
        <span><a :href="email">Email</a></span>
      </div>
      <div class="space-x-2 inline-flex">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" style="padding: 2px" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M4 4a2 2 0 012-2h4.586A2 2 0 0112 2.586L15.414 6A2 2 0 0116 7.414V16a2 2 0 01-2 2H6a2 2 0 01-2-2V4zm2 6a1 1 0 011-1h6a1 1 0 110 2H7a1 1 0 01-1-1zm1 3a1 1 0 100 2h6a1 1 0 100-2H7z" clip-rule="evenodd" />
        </svg>
        <span><a :href="resume">Resume</a></span>
      </div>
    </div>
  </div>
</template>

<script>
// import resume from '../assets/logo.png'
import resume from '../assets/resume_mid2021.pdf'

export default {
  name: 'Contact',
  setup: () => {
    const github = 'https://github.com/rnikko'
    const email = 'mailto:me@raphaelmuli.com'

    return {
      github,
      email,
      resume
    }
  }
}
</script>
