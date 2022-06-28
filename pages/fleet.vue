<template>
  <div class="container">
    <h1>HN Fleet</h1>
    <p class="lead">
      frigates, corvettes, guided missle attack craft, gunboats, minehunters,
      minesweepers, landing craft, support vessels, UAVs, anti-submarine vessels
      and submarines
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
          :characteristics="vessel.characteristics"
          :imageUrl="vessel.imageUrl"
          :tags="vessel.tags"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "fleet",
  data() {
    return {
      fleet: [
        {
          header: "Meko 200HN 'Hydra'",
          characteristics: [
            { type: "Length", value: "117.5m" },
            { type: "Displacement", value: "4,000 tons" },
            { type: "Speed", value: "31 knots" },
            {
              type: "Armament",
              value:
                '5" Mk 45, 2x Mk 15 Phalanx CIWS, 2x Mk 141 Harpoon, 2x Mk 48 VLS, 2x Mk 32 SVTT',
            },
          ],
          imageUrl: "meko-200.jpg",
          tags: [{ type: "Frigate" }, { type: "Pending MLU" }],
        },
        {
          header: "Naval Group FDI HN",
          characteristics: [
            { type: "Length", value: "122m" },
            { type: "Displacement", value: "4,460 tons" },
            { type: "Speed", value: "27 knots" },
            {
              type: "Armament",
              value:
                "Oto Melara 76mm Super Rapid, 8x Exocet MM40 blk 3, 4x Sylver A50 8-cell VLS, Mk 49 RAM blk 2, 2x EuroTorp MU90, 2x Narwhal 20mm RWS",
            },
          ],
          imageUrl: "fdi.jpg",
          tags: [{ type: "Frigate" }],
        },
        {
          header: "Standar Batch III 'Elli'",
          characteristics: [
            { type: "Length", value: "130m" },
            { type: "Displacement", value: "3,800 tons" },
            { type: "Speed", value: "30 knots" },
            {
              type: "Armament",
              value:
                "2x OTO-Melara Compatto 76mm, 2x Mk 15 Phalanx CIWS, 4x Mk 141 Harpoon blk 2, Mk 25 w/ 8x Sea Sparrow, 2x Mk 32 SVTT",
            },
          ],
          imageUrl: "standard-batch-iii.jpg",
          tags: [{ type: "Frigate" }, { type: "Pending replacement" }],
        },
        {
          header: "Roussen class 'Super Vita'",
          characteristics: [
            { type: "Length", value: "62m" },
            { type: "Displacement", value: "670 tons" },
            { type: "Speed", value: "35 knots" },
            {
              type: "Armament",
              value:
                "Oto Melara 76mm Super Rapid, 8x MM40 Exocet blk 3, Mk 49 RAM blk 2, 2x Oto Melara 30mm",
            },
          ],
          imageUrl: "super-vita.jpg",
          tags: [{ type: "Fast Attack Guided Missle Boat" }],
        },
        {
          header: "'La Combattante' IIIA",
          characteristics: [
            { type: "Length", value: "56m" },
            { type: "Displacement", value: "425 tons" },
            { type: "Speed", value: "36.5 knots" },
            {
              type: "Armament",
              value:
                "2x Oto Melara 76mm, 4x Mk 141 Harpoon blk 2, 4x Emerson Electric 30mm, 2x SST-4 torpedos",
            },
          ],
          imageUrl: "combattante-iiia.jpg",
          tags: [{ type: "Fast Attack Guided Missle Boat" }],
        },
        {
          header: "'La Combattante' IIIB",
          characteristics: [
            { type: "Length", value: "56m" },
            { type: "Displacement", value: "425 tons" },
            { type: "Speed", value: "36.5 knots" },
            {
              type: "Armament",
              value:
                "2x Oto Melara 76mm, 4x Mk 141 Harpoon blk 2, 2x Emerson Electric 30mm, 2x SST-4 torpedos",
            },
          ],
          imageUrl: "combattante-iiib.jpg",
          tags: [{ type: "Fast Attack Guided Missle Boat" }],
        },
        {
          header: "Osprey HSY 56a 'Fighter'",
          characteristics: [
            { type: "Length", value: "56m" },
            { type: "Displacement", value: "575 tons" },
            { type: "Speed", value: "23 knots" },
            {
              type: "Armament",
              value:
                "2x Oto Melara 76mm, 1x Bofors 40/70mm, 2x Rheinmetall Rh202 20mm, 2x SPIKE NLOS ATGMs",
            },
          ],
          imageUrl: "osprey-hsy-56a.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "Osprey 55",
          characteristics: [
            { type: "Length", value: "56m" },
            { type: "Displacement", value: "575 tons" },
            { type: "Speed", value: "23 knots" },
            {
              type: "Armament",
              value: "2x Oto Melara 76mm, Bofors 40mm",
            },
          ],
          imageUrl: "osprey-55.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "'La Combattante' IIA",
          characteristics: [
            { type: "Length", value: "47m" },
            { type: "Displacement", value: "265 tons" },
            { type: "Speed", value: "36 knots" },
            {
              type: "Armament",
              value:
                "Oto Melara 76mm, Bofors 57mm, Bofors 40/70mm, 4x Mk 141 Harpoon blk 2, 20x depth charges",
            },
          ],
          imageUrl: "combattante-iia.jpg",
          tags: [{ type: "Gunboat" }],
        },
        {
          header: "Type 214 'Papanikolis'",
          characteristics: [
            { type: "Length", value: "65m" },
            { type: "Displacement", value: "1,830 tons" },
            { type: "Speed", value: "20 knots" },
            {
              type: "Armament",
              value: "8x 533mm SeaHake mod 4",
            },
          ],
          imageUrl: "type-214.jpg",
          tags: [{ type: "General Purpose Submarine" }],
        },
        {
          header: "Type 209 1200AIP 'Poseidon'",
          characteristics: [
            { type: "Length", value: "64m" },
            { type: "Displacement", value: "1,810 tons" },
            { type: "Speed", value: "22 knots" },
            {
              type: "Armament",
              value: "8x 533mm torpedos",
            },
          ],
          imageUrl: "type-209.jpg",
          tags: [{ type: "General Purpose Submarine" }],
        },
        {
          header: "Etna",
          characteristics: [
            { type: "Length", value: "146m" },
            { type: "Displacement", value: "13,188 tons" },
            { type: "Speed", value: "21 knots" },
            {
              type: "Armament",
              value: "Mk 15 Phalanx CIWS, 4x Rheinmetall 20mm",
            },
          ],
          imageUrl: "etna.jpg",
          tags: [
            { type: "Naval Replenishment" },
            { type: "Logisitcs Support" },
          ],
        },
        {
          header: "LST 'Jason'",
          characteristics: [
            { type: "Length", value: "116m" },
            { type: "Displacement", value: "4,470 tons" },
            { type: "Speed", value: "16 knots" },
            {
              type: "Armament",
              value:
                "Oto Melara 76mm, 2x Bofors 40mm, 2x twin Rheinmetall Rh202 20mm",
            },
          ],
          imageUrl: "json.jpg",
          tags: [{ type: "Tank Landing Ship" }],
        },
        {
          header: "Osprey",
          characteristics: [
            { type: "Length", value: "57m" },
            { type: "Displacement", value: "895 tons" },
            { type: "Speed", value: "12 knots" },
            {
              type: "Armament",
              value: "Stinger SAM",
            },
          ],
          imageUrl: "osprey.jpg",
          tags: [{ type: "Minehunter" }],
        },
        {
          header: "Hunt",
          characteristics: [
            { type: "Length", value: "60m" },
            { type: "Displacement", value: "740 tons" },
            { type: "Speed", value: "17 knots" },
            {
              type: "Armament",
              value: "DS30M mk2 30mm",
            },
          ],
          imageUrl: "hunt.jpg",
          tags: [{ type: "Mine Countermeasure Vessel" }],
        },
        {
          header: "LCAC 'Zubr'",
          characteristics: [
            { type: "Length", value: "57m" },
            { type: "Displacement", value: "555 tons" },
            { type: "Speed", value: "63 knots" },
            {
              type: "Armament",
              value: "2x AK-630 CIWS, 2x 140mm Ogon launchers, 4x Strela-3 SAM",
            },
          ],
          imageUrl: "zubr.jpg",
          tags: [{ type: "Landing Craft" }],
        },
        {
          header: "Lockheed P-3B 'Orion'",
          characteristics: [
            { type: "Length", value: "35m" },
            { type: "Speed", value: "411 knots" },
            { type: "Service ceiling", value: "28,300 ft" },
            {
              type: "Armament",
              value: "8x Mk 46, 7x MU-90, Active/Passive Sonobuoys",
            },
          ],
          imageUrl: "p-3.jpg",
          tags: [{ type: "Anti-submarine" }],
        },
        {
          header: "Sikorsky SH-70B6/MH-60R Aegean Hawk",
          characteristics: [
            { type: "Speed", value: "146 knots" },
            { type: "Service ceiling", value: "12,000 ft" },
            {
              type: "Armament",
              value: "2x Mk 46, 4x AGM-114",
            },
          ],
          imageUrl: "s-70b.jpg",
          tags: [{ type: "Anti-submarine" }],
        },
        {
          header: "Alpha A900 UAV",
          characteristics: [],
          imageUrl: "a900.jpg",
          tags: [{ type: "UAV" }, { type: "Surveillance" }],
        },
      ],
    };
  },
};
</script>
