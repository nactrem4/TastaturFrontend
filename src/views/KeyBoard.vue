<template>
  <h1>Welcome to your next Keyboard</h1>
  <div class="container-fluid">
    <div class="row row-cols-1 row-cols-md-4 g-4">
      <div class="col" v-for="keyboard in keyboards" :key="keyboard.id">
        <div class="card h-100 .bg-image hover-zoom">
          <img :src=" keyboard.keyboardImage " class ="w-100" >
        </div>
          <div class="card-body">
            <h5 class="card-title">{{ keyboard.keyboardName }} </h5>
            <p class="card-text"> {{keyboard.keyboardBeschreibung}} </p>
            <p class="card-text"> {{keyboard.keyboardPreis}} </p>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Keyboards',
  data () {
    return {
      keyboards: [
        {
          id: 1,
          keyboardName: 'Tofu 60',
          keyboardBeschreibung: 'Budget Einsteiger mit einem sehr dünnen Soundprofil',
          keyboardPreis: '160 Euro',
          keyboardImage: 'https://kbdfans.com/cdn/shop/files/12_790c9fc7-3d00-43f0-b890-26b815fe8f84_720x.jpg?v=1709373883'
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>

<!--
 Quelle : https://kbdfans.com/products/tofu60-2-0
 Test -->
