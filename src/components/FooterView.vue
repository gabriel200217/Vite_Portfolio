<template>
  <v-footer style="background: rgb(9, 45, 83)">
     <v-card elevation="0" rounded="0" width="100%" class="bg-black text-center">
         <v-card-text>
             <a href="https://www.facebook.com/profile.php?id=100052271462353" target="blank">
                <v-btn class="mw-4" icon="fas fa-comment" variant="plain" color="white"></v-btn>
             </a>
             <!-- https://github.com/gabriel200217 -->
             <a href="https://github.com/gabriel200217" target="blank">
               <v-btn class="mx-4" icon="fas fa-brands fa-github" variant="plain" color="white"></v-btn>
             </a>
             <a href="https://www.linkedin.com/in/gabriel-chacon-39a882200/" target="blank">
                <v-btn class="mx-4" icon="fas fa-brands fa-linkedin" variant="plain" color="white"></v-btn>
             </a>
             <a href="http://www.iujobarquisimeto.edu.ve" target="blank">
                <v-btn class="mx-4" icon="fas fa-university" variant="plain" color="white"></v-btn>
             </a>
         </v-card-text>
         <v-card-text class="text-white">
             @ {{new Date().getFullYear()}}
             <strong> - All rights reserved</strong>
         </v-card-text>
     </v-card>
  </v-footer>
</template>

<script>
export default {

}
</script>

<style>
.v-footer{
   padding: 8px 0 !important;
}
</style>