<template>
  <div class="container">
    <h1>HN Fleet</h1>
    <p class="lead">
      frigates, corvettes, fast-attack missle boats, gunboats and submarines
    </p>
    <hr />
    <div
      class="
        row
        row-cols-1
        row-cols-xxl-4
        row-cols-xl-3
        row-cols-lg-2
        row-cols-md-2
        row-cols-sm-1
        g-4
        mb-4
      "
    >
      <div class="col" v-for="vessel in fleet" :key="vessel.id">
        <Card
          :header="vessel.header"
          :description="vessel.description"
          :imageUrl="vessel.imageUrl"
          :tags="vessel.tags"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Fleet",
  data() {
    return {
      fleet: [
        {
          header: "Meko 200HN 'Hydra'",
          description: "Friagte",
          imageUrl: "meko-200.jpg",
          tags: [{ type: "Frigate" }],
        },
        {
          header: "Standar Batch III 'Elli'",
          description: "",
          imageUrl: "standard-batch-iii.jpg",
          tags: [{ type: "Frigate" }],
        },
        {
          header: "Roussen class 'Super Vita'",
          description: "",
          imageUrl: "super-vita.jpg",
          tags: [{ type: "Fast Attack Missle Boat" }],
        },
        {
          header: "Osprey HSY 56a 'Fighter'",
          description: "",
          imageUrl: "osprey-hsy-56a.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "Naval Group FDI HN",
          description: "",
          imageUrl: "fdi.jpg",
          tags: [{ type: "Frigate" }],
        },
        {
          header: "Naval Group Gowind",
          description: "",
          imageUrl: "gowind.jpg",
          tags: [{ type: "Corvette" }, { type: "TBA" }],
        },
        {
          header: "Fincantieri Multirole Corvette",
          description: "",
          imageUrl: "fincantieri.jpg",
          tags: [{ type: "Corvette" }, { type: "TBA" }],
        },
        {
          header: "'Alreigh Burke'",
          description: "",
          imageUrl: "alreigh-burke.jpg",
          tags: [{ type: "Guided Missle Destroyer" }, { type: "TBA" }],
        },
        {
          header: "Hellenic Future Friagte 'HF2'",
          description: "",
          imageUrl: "hf2.jpg",
          tags: [{ type: "Frigate" }, { type: "TBA" }],
        },
        {
          header: "Type 214 'Papanikolis'",
          description: "",
          imageUrl: "type-214.jpg",
          tags: [{ type: "General Purpose Submarine" }],
        },
      ],
    };
  },
};
</script>
