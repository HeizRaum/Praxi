<template>
  <li class="listElement">
    <h3 v-bind:class="{ active: showContent }">{{title}}</h3>
    <div class="elementContent" v-if="showContent">
      testing
    </div>
  </li>
</template>

<script lang="ts">
interface ListElement {
  title: string;
  showContent: boolean;
}

export default {
  setup() {
    return {};
  },
  props: {
    title: String,
    showContent: Boolean,
  },
};
</script>

<style lang="scss" scoped>
h3 {
  font-family: 'Source Sans Pro';
  font-size: 16pt;

  background-color: $white0;
  padding: 1rem;
  margin-bottom: 5px;

  border: 2px solid $gray0;
  border-radius: 10px;
  box-shadow: 0px 5px 0px $gray0;
  -webkit-user-select: none;
}
h3.active {
  transform: translateY(5px);
  box-shadow: none;
}
.listElement {
  margin: 2rem;
  list-style-type: none;
  .elementContent {
    font-family: 'PT Mono', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 12pt;

    background: $white0;

    padding-top: 1rem;
    padding-bottom: 0.5rem;
    margin-left: 3rem;
    margin-right: 3rem;

    border-radius: 0 0 10px 10px;
  }
}
</style>
