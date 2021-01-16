<template web>
  <div class="page-about">
    <section class="hero">
      <div class="hero-content">
        <h1>
          We are community
        </h1>
        <p>
          We are a community full of people passionate about sharing experiences
          and exchanging knowledge
        </p>
        <button>Join our community</button>
      </div>
      <div class="hero-img" />
    </section>
    <section class="info">
      <div class="info-img" />
      <p>
        Maecenas lorem. Proin in tellus sit amet nibh dignissim sagittis.
        Praesent dapibus. Ut enim ad minima veniam, quis nostrum exercitationem
        ullam corporis suscipit
      </p>
    </section>
    <section class="team">
      <h2>
        Meet <br />
        our team
      </h2>
      <div class="members">
        <figure class="member" v-for="member in members" :key="member.name">
          <img
            class="member-img"
            :src="
              member.avatar ? member.avatar : '../assets/avatar-placeholder.jpg'
            "
            :alt="member.name"
          />
          <figcaption class="member-details">
            <div class="member-name" v-text="member.name" />
            <div
              class="member-position"
              v-if="member.position"
              v-text="member.position"
            />
          </figcaption>
        </figure>
      </div>
    </section>
    <c2a-download />
  </div>
</template>
<script>
import C2aDownload from "../components/C2aDownload.vue";

export default {
  components: {
    C2aDownload
  },
  data: () => ({
    members: [
      {
        name: "Iina Jutila",
        position: "Big boss",
        avatar:
          "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80"
      },
      {
        name: "Katherine Moss",
        position: "Developer"
      },
      {
        name: "Larry Lin",
        avatar:
          "https://images.unsplash.com/photo-1557296387-5358ad7997bb?ixid=MXwxMjA3fDB8MHxzZWFyY2h8M3x8ZmFjZXxlbnwwfHwwfA%3D%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
      }
    ]
  })
};
</script>

<style lang="scss" scoped>
.hero {
  align-items: center;
  background-color: #f1f2f6;
  display: flex;
  justify-content: center;
  padding: 50px;

  &-content {
    width: 50%;

    h1 {
      font-size: 56px;
      font-weight: bold;
      margin-bottom: 20px;
    }

    p {
      font-size: 20px;
      font-weight: semi-bold;
      margin-bottom: 50px;
    }
  }

  &-img {
    background-image: url("https://images.unsplash.com/photo-1490578474895-699cd4e2cf59?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OXx8dHJhdmVsJTIwZ3JvdXB8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 550px;
    width: 50%;
  }
}

.info {
  align-items: center;
  display: flex;
  justify-content: center;
  padding: 150px 50px;

  &-img {
    background-image: url("https://images.unsplash.com/photo-1455849318743-b2233052fcff?ixid=MXwxMjA3fDB8MHxzZWFyY2h8OHx8dHJhdmVsJTIwZ3JvdXB8ZW58MHx8MHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    height: 550px;
    width: 50%;
  }

  p {
    margin-left: 30px;
    font-size: 32px;
  }
}

.team {
  background-color: #f1f2f6;
  padding: 150px 50px;

  h2 {
    font-size: 46px;
    margin-bottom: 80px;
  }

  .members {
    align-items: center;
    display: flex;
    justify-content: flex-start;
    gap: 30px;

    .member {
      align-items: center;
      display: flex;
      justify-content: flex-start;
      gap: 15px;

      &-img {
        border-radius: 50%;
        height: 90px;
        object-fit: cover;
        width: 90px;
      }

      &-name {
        font-size: 18px;
        font-weight: semi-bold;
      }

      &-position {
        margin-top: 5px;
      }
    }
  }
}
</style>
