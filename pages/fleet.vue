<template>
  <div class="container">
    <h1>HN Fleet</h1>
    <p class="lead">
      frigates, corvettes, fast-attack guided missle boats, gunboats,
      minehunter, minesweepers, landing craft, support vessels, UAVs,
      Anti-submarine vessels and submarines
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
          header: "Naval Group FDI HN",
          description: "",
          imageUrl: "fdi.jpg",
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
          tags: [{ type: "Fast Attack Guided Missle Boat" }],
        },
        {
          header: "'La Combattante' IIIA",
          description: "",
          imageUrl: "combattante-iiia.jpg",
          tags: [{ type: "Fast Attack Guided Missle Boat" }],
        },
        {
          header: "'La Combattante' IIIB",
          description: "",
          imageUrl: "combattante-iiib.jpg",
          tags: [{ type: "Fast Attack Guided Missle Boat" }],
        },
        {
          header: "Osprey HSY 56a 'Fighter'",
          description: "",
          imageUrl: "osprey-hsy-56a.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "Osprey 55",
          description: "",
          imageUrl: "osprey-55.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "'La Combattante' IIA",
          description: "",
          imageUrl: "combattante-iia.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "Naval Group Gowind",
          description: "",
          imageUrl: "gowind.jpg",
          tags: [{ type: "Corvette" }, { type: "TBA" }],
        },
        {
          header: "Damen Group Sigma",
          description: "",
          imageUrl: "sigma.jpg",
          tags: [{ type: "Corvette" }, { type: "TBA" }],
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
        {
          header: "Naval Replenishment 'Etna'",
          description: "",
          imageUrl: "etna.jpg",
          tags: [
            { type: "Naval Replenishment" },
            { type: "Logisitcs Support" },
          ],
        },
        {
          header: "'Jason' LST",
          description: "",
          imageUrl: "json.jpg",
          tags: [{ type: "Tank Landing Ship" }],
        },
        {
          header: "LCU 520",
          description: "",
          imageUrl: "lcu-520.jpg",
          tags: [{ type: "Landing Ship" }],
        },
        {
          header: "Osprey",
          description: "",
          imageUrl: "osprey.jpg",
          tags: [{ type: "Minehunter" }],
        },
        {
          header: "'Hunt'",
          description: "",
          imageUrl: "hunt.jpg",
          tags: [{ type: "Mine Countermeasure" }],
        },
        {
          header: "'Zubr'",
          description: "",
          imageUrl: "zubr.jpg",
          tags: [{ type: "Landing Craft" }],
        },
        {
          header: "Lockheed P-3B Orion",
          description: "",
          imageUrl: "p-3.jpg",
          tags: [{ type: "Anti-submarine" }],
        },
        {
          header: "Sikorsky S-70B 'Aegean Hawk'",
          description: "",
          imageUrl: "s-70b.jpg",
          tags: [{ type: "Anti-submarine" }],
        },
        {
          header: "A900",
          description: "",
          imageUrl: "a900.jpg",
          tags: [{ type: "UAV" }, { type: "Surveillance" }],
        },
      ],
    };
  },
};
</script>
