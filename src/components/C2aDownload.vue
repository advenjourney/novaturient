<template>
  <section class="c2a-download">
    <h2>Download our app</h2>
    <p>
      We love what we do and we do what our clients love & work with great
      clients all over the world to create thoughtful and purposeful websites
    </p>
    <div class="c2a-download-actions">
      <button>iOS</button>
      <button>Android</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "C2aDownload"
};
</script>

<style lang="scss" scoped>
.c2a-download {
  background-color: #f5f5f5;
  padding: 150px 50px;
  text-align: center;

  h2 {
    color: #091d36;
    font-size: 46px;
    margin-bottom: 20px;
  }

  p {
    color: #0b4c84;
    font-size: 20px;
    margin-bottom: 60px;
  }

  &-actions {
    button + button {
      margin-left: 20px;
    }
  }
}
</style>
