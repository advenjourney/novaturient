<template>
  <footer class="footer">
    <span class="footer-copy">Made by Advenjourney</span>
    <div class="footer-socials">
      <a
        v-for="social in socials"
        :key="social.name"
        :href="social.link"
        :title="social.name"
        target="_blank"
      >
        <img
          :src="`../assets/icon-${social.name.toLowerCase()}.svg`"
          aria-hidden="true"
        />
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "VHeader",

  data: () => ({
    socials: [
      {
        name: "Facebook",
        link: "http://facebook.com/advenjourney"
      },
      {
        name: "Twitter",
        link: "http://twitter.com/advenjourney"
      },
      {
        name: "Instagram",
        link: "http://instagram.com/advenjourney"
      },
      {
        name: "GitHub",
        link: "http://github.com/advenjourney/novaturient"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
.footer {
  align-items: center;
  display: flex;
  justify-content: space-between;
  height: 120px;
  padding: 0 50px;

  &-socials {
    a + a {
      margin-left: 20px;
    }
  }
}
</style>
