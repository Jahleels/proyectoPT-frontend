<template>
  <v-card class="mx-auto" max-width="100vw">
    <v-card-text>
      <div>Word of the Day</div>
      <p class="text-h4 text--primary">
        el·ee·mos·y·nar·y
      </p>
      <p>adjective</p>
      <div class="text--primary">
        relating to or dependent on charity; charitable.<br />
        "an eleemosynary educational institution."
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "AdminHello",
  data: () => ({
    reveal: false,
  }),
};
</script>

<style>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
</style>
