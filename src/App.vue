<template>
     <Navbar />
     <Welcome />
     <section id="about">
          <h1>What is Pop it exactly?</h1>
          <p>This is a child game, in which the process can be compared to the burstring of a bubble wrap. But unlike film, pop-it can be pressed with the seme characteristic sensations and sounds "endlessy": dozens of silicone bubbles are simply squeezed out in the other direction.</p>
     </section>
</template>
<script setup>
import Navbar from "./components/Navbar.vue";
import Welcome from "./components/Welcome.vue";
</script>

<style scoped>
#about {
     width: 100%;
     text-align: center;
     padding: 100px 0px;
     display: flex;
     flex-flow: column;
     align-items: center;
     justify-content: center;
}

#about h1 {
     font-size: 30px;
     font-weight: 800;
     margin: 0;
}

#about p {
     font-size: 20px;
     font-weight: 100;
     max-width: 60%;
     margin: 20px 0px 0px 0px;
}

@media only screen and (max-width: 720px) {
     #about h1 {
          font-size: 25px;
     }

     #about p {
          font-size: 18px;
     }
}
</style>
