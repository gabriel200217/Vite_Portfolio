<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn icon>
      <!-- <font-awesome-icon icon="fa-sharp fa-solid fa-galaxy" /> -->
      <v-icon color="red" left class="mr-2">fas fa-hurricane</v-icon>Gabriel
    </v-btn>
    <v-spacer></v-spacer>
    <a href="#Home" style="text-decoration: none">
      <v-btn text @click="scroll(home)" class="text-red" id="Init">Home</v-btn>
    </a>
    <a href="#About" style="text-decoration: none">
      <v-btn text @click="scroll(about)" class="text-red" id="Aabout">About</v-btn>
    </a>
    <a href="#portfolio" style="text-decoration: none">
      <v-btn text @click="scroll(portfolio)" class="text-red" id="Port">Portfolio</v-btn>
    </a>
    <a href="#page" style="text-decoration: none">
      <v-btn text @click="scroll(services)" class="text-red" id="Proyects">Proyects</v-btn>
    </a>
    <a href="#TextPHP" style="text-decoration: none">
      <v-btn text @click="scroll(page)" class="text-red" id="Description">Description</v-btn>
    </a>
    <a href="#contact" style="text-decoration: none">
      <v-btn text @click="scroll(contacts)" class="text-red" id="Contacts">Contacts</v-btn>
    </a>
  </v-app-bar>
</template>

<script>

export default {
  methods: {
    scroll(refName) {
      const element = document.getElementsById(refName)
      element.scrollIntoView({behavior: "smooth"})
    }
  }
}
</script>

<style>
*{
  scroll-behavior: smooth;
}
</style>