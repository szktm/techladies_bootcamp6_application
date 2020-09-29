<template>
  <div> 
    <h3>tomoe's corner of the internet</h3> 
    <nav> 
      <router-link v-for ="routes in links" class="spacing"
      v-bind:key="routes.id"
      :to="`${routes.page}`">{{routes.text}}</router-link>
    </nav> 
  </div>
</template>

<script>
  export default {
    name: 'Navigation',
    data() {
      return {
        links: [
          {
            id: 0,
            text: 'Home',
            page:'/Home'
          },
          {
            id: 1,
            text: 'About',
            page:'/About'
          },
          {
            id: 2,
            text: 'Contact',
            page:'/Contact'
          },
      
          
        ]
      }
    }
  }
</script>


<style> 
  .spacing { 
    margin-left: 10px; 
  } 
</style>