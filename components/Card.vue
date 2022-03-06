<template>
  <div class="card" style="width: 18rem">
    <a :href="require(`@/assets/images/${imageUrl}`)" target="_blank">
      <img
        :src="require(`@/assets/images/${imageUrl}`)"
        class="card-img-top"
        :alt="header"
        :title="header"
      />
    </a>
    <div class="card-body pb-0">
      <h4 class="card-title mb-0">{{ header }}</h4>
      <h5 class="mt-2 mb-0 font-weight-bold">Specs</h5>
      <ul class="p-0 mb-0" style="list-style-position: inside; list-style: none">
        <li v-for="characteristic in characteristics" :key="characteristic.id">
          <span class="font-weight-bold">{{ characteristic.type }}:</span>
          <span>{{ characteristic.value }}</span>
        </li>
      </ul>
    </div>
    <div class="card-footer">
      <Badge
        v-for="tag in tags"
        :key="tag.id"
        :text="tag.type"
        color="primary"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    imageUrl: {
      type: String,
      required: true,
    },
    header: {
      type: String,
      required: true,
    },
    characteristics: {
      type: Array,
      required: true,
    },
    tags: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>
