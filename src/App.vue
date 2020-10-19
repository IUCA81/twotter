<template>
  <div class="app">
    <div>
      @{{ user.username }} - {{ fullName }}
    </div>
    <p>
      <strong>Followers: </strong> {{ followers }}
    </p>
    <button @click="followUser">Follow</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: '_IulianCazan',
        firstName: 'Iulian',
        lastName: 'Cazan',
        email: 'jaybliss@gmail.com',
        isAdmin: true
      }
    }
  },
  watch: {

  },
  computed: {
      fullName() {
        return `${this.user.firstName} ${this.user.lastName}`;
      }
  },
  methods: {
    followUser() {
      this.followers ++;
    }
  },
  mounted() {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  flex-direction: column;
}
</style>
