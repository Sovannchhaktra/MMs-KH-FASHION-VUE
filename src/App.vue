<script>
import {ref,computed} from 'vue'

    import Navbar from "@/components/navbar/index.vue";
    import Footer from "@/components/footer/index.vue";
    import Sidebar from "@/components/sidebar/index.vue"
    export default {
      name: "App",
      components: {
        Navbar,
        Footer,
        Sidebar
      },
      data() {
        
      },
      mounted() {
        const token = "12345abcde";
        sessionStorage.setItem("accessToken", token);
      },
    };
</script>
<template>
  <main id="app" class="w-100 h-auto flex flex-col items-center">
    <Navbar />
    <div class="w-full fixed h-auto top-[3.9rem] flex gap-10">
      <div>
        <Sidebar />
      </div>
      <RouterView />
    </div>
    <!-- <Footer /> -->
  </main>
</template>


<style>
body {
  background-color: white;
}
</style>
