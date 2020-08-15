<template>
  <div>
    <h1>Let's get in touch</h1>
 <h3>
      Hi there! 👋
      <br>
      You can reach me via email at {{email}}, or on Telegram at {{telegram}}. 
      <br>
      Alternatively, we can meet up for coffee or mala (it's a team sport!) sometime.
  </h3>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data(){
    return {
      email: "suzukitomoe@u.nus.edu",
      telegram: "@szktm"
    }
  }
}
</script>