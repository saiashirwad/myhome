<script setup lang="ts">
// Define your social links
const SOCIALS = [
  { NAME: 'Twitter', HREF: 'https://x.com/texoport__' },
  { NAME: 'Bluesky', HREF: 'https://bsky.social/texoport' },
  // Add other social links as needed
]
</script>

<template>
  <div class="container">
    <aside>
      <div class="space-y">
        <section>
          <article class="intro">
            <span>
              <p>
                Hi, I'm Sai, and I go by
                <a href="https://bsky.social/texoport" target="_blank">texoport</a>
                online, where I'm known for being a
                <a
                  href="https://x.com/texoport__/status/1849231907214762003"
                  target="_blank"
                >type-level Typescript addict</a>.
              </p>
              <p>
                I'm currently working on
                <a href="https://outroute.co" target="_blank">Outroute</a>, a
                Route Optimization platform that I'm a co-founder of.
              </p>
              <p>
                I was a student at BITS Pilani, focusing on Deep Learning and
                Knowledge Graphs during for my thesis.
              </p>
              <p>
                As of the last year, I've been enamored by the world of PL and
                type theory.
              </p>
            </span>
          </article>
        </section>

        <section class="socials">
          <h2>My usual haunts</h2>
          <ul>
            <li v-for="social in SOCIALS" :key="social.NAME">
              <a
                :href="social.HREF"
                target="_blank"
                :aria-label="`Visit ${social.NAME}`"
              >
                {{ social.NAME }}
              </a>
            </li>
          </ul>
        </section>
      </div>
    </aside>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2rem;
}

.space-y {
  display: flex;
  flex-direction: column;
  gap: 4rem;
}

.intro {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.intro p {
  line-height: 1.6;
}

.intro a {
  color: #0066cc;
  text-decoration: none;
}

.intro a:hover {
  text-decoration: underline;
}

h2 {
  font-weight: 600;
  margin-bottom: 1rem;
}

.socials ul {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  list-style: none;
  padding: 0;
}

.socials a {
  color: #0066cc;
  text-decoration: none;
}

.socials a:hover {
  text-decoration: underline;
}
</style>