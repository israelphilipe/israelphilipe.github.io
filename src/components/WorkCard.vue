<template>
  <q-card class="q-mb-md">
    <q-badge
      v-if="work.current"
      class="text-h6 text-bold q-px-lg"
      style="border-radius: 15px"
      floating
      color="green"
    >
      Current
    </q-badge>
    <q-card-section class="text-h5">
      <div class="row items-center">
        <q-avatar square size="3em" class="q-mr-md">
          <img :src="work.establishment.image" />
        </q-avatar>
        {{ work.establishment.title }}
      </div>
    </q-card-section>
    <q-card-section class="text-h6">
      {{ work.establishment.title }}
    </q-card-section>
    <q-card-section class="text-h6">
      {{ work.establishment.description }}
    </q-card-section>

    <q-card-section class="text-h6"> {{ work.work_description }} </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: ["work"],
};
</script>

<style></style>
