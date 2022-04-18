<template>

  <NavBar/>
  <router-view/>

  <!-- <div class="container mt-3">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p class="h3 text-success fw-bold">App Component</p>
          <p class="fw-bold">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Saepe dolor commodi eligendi! Labore laborum, molestiae eaque odio in accusantium atque impedit tempora distinctio esse blanditiis eligendi numquam repellat, dignissimos nemo.</p>
        </div>
      </div>
    </div> -->

    <!-- <Register/> -->
    <!-- <AuthUser/> -->
    <!-- <Spinner/> -->
    <!-- <UserList/> -->

  <!-- </div> -->
</template>

<script>
// import UserList from "@/components/UserList";
// import Spinner from "@/components/Spinner.vue";
import NavBar from "@/components/NavBar.vue"

export default {
  components: { NavBar }
}
</script>

<style scoped>
  @import "./styles.css";
</style>