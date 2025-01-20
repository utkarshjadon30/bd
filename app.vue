<template>
  <!-- <div >

    <v-row>



    </v-row>
    <h3>Are you the best sage in the world????</h3>
    <v-btn variant="outlined">Hello</v-btn>
  </div> -->
  <v-container
    fluid
    v-if="!nobool"
    class="bg-black text-white"
    style="height: 100vh"
  >
    <v-card class="mx-auto my-12" max-width="600">
      <v-img
        class="align-end text-white"
        height="400"
        src="/images/sage2.webp"
        cover
      >
      </v-img>

      <v-card-subtitle class="pt-4"> Number 0 </v-card-subtitle>

      <v-card-text>
        <div>Deepanshi Rawat</div>

        <div>Are you the best sage in the world????</div>
        <div class="text-red" v-if="yesmessagebool">{{ yesmessage }}</div>
      </v-card-text>

      <v-card-actions>
        <v-btn color="black" text="Yes" @click="yesclick"></v-btn>

        <v-btn color="black" text="No" @click="nobool = true"></v-btn>
      </v-card-actions>
    </v-card>
  </v-container>
  <v-container
    fluid
    v-if="nobool"
    class="bg-black text-white"
    style="height: 100vh"
  >
    <v-row>
      <v-col v-for="i in jsondata">
        <v-card
          class="text-white"
          color="#26c6da"
          max-width="600"
          prepend-icon="mdi-twitter"
          title="Twitter"
        >
          <template v-slot:prepend>
            <v-icon size="x-large"></v-icon>
          </template>

          <v-card-text class="text-h5 py-2">{{ i.msg }} </v-card-text>

          <v-card-actions>
            <v-list-item class="w-100">
              <template v-slot:prepend>
                <v-avatar
                  color="grey-darken-3"
                  image="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                ></v-avatar>
              </template>

              <v-list-item-title>{{ i.name }}</v-list-item-title>

              <v-list-item-subtitle>{{ i.title }}</v-list-item-subtitle>

              <template v-slot:append>
                <div class="justify-self-end">
                  <v-icon class="me-1" icon="mdi-heart"></v-icon>
                  <span class="subheading me-2">256</span>
                  <span class="me-1">·</span>
                  <v-icon class="me-1" icon="mdi-share-variant"></v-icon>
                  <span class="subheading">45</span>
                </div>
              </template>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col v-for="i in jsondata2">
        <v-card
          class="text-white"
          color="#26c6da"
          max-width="600"
          prepend-icon="mdi-twitter"
          title="Twitter"
        >
          <template v-slot:prepend>
            <v-icon size="x-large"></v-icon>
          </template>

          <v-card-text class="text-h5 py-2">{{ i.msg }} </v-card-text>

          <v-card-actions>
            <v-list-item class="w-100">
              <template v-slot:prepend>
                <v-avatar
                  color="grey-darken-3"
                  image="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                ></v-avatar>
              </template>

              <v-list-item-title>{{ i.name }}</v-list-item-title>

              <v-list-item-subtitle>{{ i.title }}</v-list-item-subtitle>

              <template v-slot:append>
                <div class="justify-self-end">
                  <v-icon class="me-1" icon="mdi-heart"></v-icon>
                  <span class="subheading me-2">256</span>
                  <span class="me-1">·</span>
                  <v-icon class="me-1" icon="mdi-share-variant"></v-icon>
                  <span class="subheading">45</span>
                </div>
              </template>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col v-for="i in jsondata3">
        <v-card
          class="text-white"
          color="#26c6da"
          max-width="600"
          prepend-icon="mdi-twitter"
          title="Twitter"
        >
          <template v-slot:prepend>
            <v-icon size="x-large"></v-icon>
          </template>

          <v-card-text class="text-h5 py-2">{{ i.msg }} </v-card-text>

          <v-card-actions>
            <v-list-item class="w-100">
              <template v-slot:prepend>
                <v-avatar
                  color="grey-darken-3"
                  image="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                ></v-avatar>
              </template>

              <v-list-item-title>{{ i.name }}</v-list-item-title>

              <v-list-item-subtitle>{{ i.title }}</v-list-item-subtitle>

              <template v-slot:append>
                <div class="justify-self-end">
                  <v-icon class="me-1" icon="mdi-heart"></v-icon>
                  <span class="subheading me-2">256</span>
                  <span class="me-1">·</span>
                  <v-icon class="me-1" icon="mdi-share-variant"></v-icon>
                  <span class="subheading">45</span>
                </div>
              </template>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
const yesmessage = ref(
  "No you are not the best sage in the world.Please click No"
)
const yesmessagebool = ref(false)
const nobool = ref(false)
const yesclick = () => {
  yesmessagebool.value = true
}

const jsondata = ref([
  {
    name: "Sentinal",
    title: "Vyse",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Duelist",
    title: "Ryena",
    msg: "Happy birthday @deepanshi",
  },

  {
    name: "Controller",
    title: "Viper",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Initiator",
    title: "Kayo",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Sentinal",
    title: "Cypher",
    msg: "Happy birthday @deepanshi",
  },
])
const jsondata2 = ref([
  {
    name: "Sentinal",
    title: "KillJoy",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Duelist",
    title: "Raze",
    msg: "Happy birthday @deepanshi",
  },

  {
    name: "Controller",
    title: "omen",
    msg: "Janam din muabrak to ther worst sage i have ever played with. I think you should leave the valo before valo leaves you. And of course you are not the best duo of mine.",
  },
  {
    name: "Initiator",
    title: "Sova",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Sentinal",
    title: "Deadlock",
    msg: "Happy birthday @deepanshi",
  },
])
const jsondata3 = ref([
  {
    name: "Sentinal",
    title: "Chamber",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Duelist",
    title: "Yoru",
    msg: "Happy birthday @deepanshi",
  },

  {
    name: "Controller",
    title: "Brim",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Initiator",
    title: "Fade",
    msg: "Happy birthday @deepanshi",
  },
  {
    name: "Duelist",
    title: "neon",
    msg: "Happy birthday @deepanshi",
  },
])
</script>

<style scoped>
.background-container {
  background-image: url("/images/Sage.webp"); /* Adjust the path if necessary */
  background-size: cover; /* Ensures the image covers the entire container */

  width: 100%; /* Full width */
  height: 100vh; /* Full viewport height */
}
</style>
