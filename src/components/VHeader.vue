<template>
  <header class="header">
    <span>Advenjourney</span>
    <nav class="navigation">
      <ul class="navigation-list">
        <li
          class="navigation-list-item"
          v-for="route in routes"
          :key="route.name"
        >
          <router-link
            class="navigation-list-link"
            :to="route.path"
            v-text="route.name"
          />
        </li>
      </ul>
    </nav>
    <button>Sign in</button>
  </header>
</template>

<script>
import { routes } from "../router/index";

export default {
  name: "VHeader",

  computed: {
    routes() {
      return routes;
    }
  }
};
</script>

<style lang="scss" scoped>
.header {
  align-items: center;
  display: flex;
  justify-content: space-between;
  height: 50px;
  padding: 0 50px;
}

.navigation-list {
  align-items: center;
  display: flex;
  list-style: none;
  justify-content: center;

  &-item + &-item {
    margin-left: 15px;
  }

  &-link {
    font-size: 18px;
    text-decoration: none;
  }
}
</style>
