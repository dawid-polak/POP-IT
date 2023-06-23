<template>
     <footer id="footer">
          <ul>
               <li>NOT_A_BUBBLE.COM</li>
               <li>Payment methods</li>
               <li>Delivery</li>
               <li>Wholesale</li>
               <li>Contacts</li>
          </ul>
     </footer>
</template>

<script setup></script>

<style scoped>
#footer {
     width: 100%;
     background-color: #333333;
     color: #fff;
}

#footer ul {
     margin: 0;
     padding: 0;
     list-style: none;
     display: flex;
     justify-content: space-around;
     flex-wrap: wrap;
}

#footer ul li {
     padding: 20px 5px 20px 5px;
     font-weight: 100;
}

#footer ul li:first-child {
     font-weight: 900;
}

/* breakpoints */
@media only screen and (max-width: 720px) {
     #footer ul li {
          width: 90%;
          text-align: center;
     }
}
</style>
