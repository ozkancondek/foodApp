<template>
  <nav>
    <ul>
      <li>
        <nuxt-link exact to="/">Home </nuxt-link>
      </li>
      <li>
        <nuxt-link exact to="/restaurants">Restaurants</nuxt-link>
      </li>
    </ul>
    <nuxt-link to="/cart"
      >cart <sup>{{ productCount }}</sup>
    </nuxt-link>
  </nav>
</template>

<script>
import { computed } from "vue";
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["productCount"]),
  },
};
</script>

<style lang="scss" scoped></style>
