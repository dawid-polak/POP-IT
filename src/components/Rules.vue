<template>
     <section id="rules">
          <img class="rules--imgbg" src="../assets/img/bg-grid.png" alt="bg-grid" />
          <div class="rules--content">
               <div class="rules--content-description">
                    <h1>Rules of the game</h1>
                    <p>
                         Players take turn and click on the bumps. It is imperative to finish the row that you started. You can press maximum of 3 bubbles at the same time (they must be near, you cannot press severl pimples at once, it they are not close to each other) The task is to make the
                         opponent the last. Who went last - he lost.
                    </p>
               </div>
               <img class="rules--content-img" src="../assets/img/photo.jpg" alt="photo" />
          </div>
     </section>
</template>

<script setup></script>

<style scoped>
#rules {
     width: 100%;
     height: 70vh;
     display: flex;
     margin-top: 100px;
}

#rules .rules--imgbg {
     margin: auto;
     object-fit: cover;
     width: 100%;
     height: 70%;
}

#rules .rules--content {
     width: 100%;
     height: 50%;
     position: absolute;
     display: flex;
     align-items: center;
     max-width: 90%;
}

#rules .rules--content .rules--content-description {
     margin: 0px 80px 0px 120px;
}
#rules .rules--content .rules--content-description h1 {
     font-size: 30px;
     font-weight: 900;
}

#rules .rules--content .rules--content-description p {
     margin-top: 40px;
     font-weight: 100;
     font-size: 20px;
}

#rules .rules--content-img {
     width: 35%;
}

/* breakpoints */

@media only screen and (max-width: 820px) {

     #rules {
          height: 120vh;
     }
     #rules .rules--content {
          flex-wrap: wrap;
          max-width: 100%;
     }

     #rules .rules--content .rules--content-description {
          margin: 0px 60px;
     }

     #rules .rules--content-img {
          width: 90%;
          margin: auto;
          margin-top: 50px;
     }
}
</style>
