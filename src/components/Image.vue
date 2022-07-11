<template>
  <div class="hello">
    <div>
      <h1>{{ title }}</h1>
      <h2>{{ msg }}</h2>
    </div>
    <div>

      <button @click="randomImage" class="btn" style="margin-left: 1rem">Next</button>
    </div>
    <div style="margin-top: 1rem">

      <img :src="selectedImage" class="image" alt="story tell"/>
      <img :src="selectedImage2" class="image" alt="story tell"/>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String,
    msg: String,
  },
  data() {
    return {
      index: 0,
      image: [
        this.importImage("1.jpg"),
        this.importImage("2.jpg"),
        this.importImage("3.jpg"),
        this.importImage("4.jpg"),
        this.importImage("5.jpg"),
        this.importImage("6.jpg"),
        this.importImage("7.jpg"),
        this.importImage("8.jpg"),
        this.importImage("10.jpg"),
        this.importImage("11.jpg"),
        this.importImage("12.jpg"),
        this.importImage("13.jpg"),
        this.importImage("14.jpg"),
        this.importImage("15.jpg"),
        this.importImage("16.jpg"),
        this.importImage("17.jpg"),
        this.importImage("18.jpg"),
        this.importImage("19.jpg"),
        this.importImage("20.jpg"),
        this.importImage("21.jpg"),
        this.importImage("22.jpg"),
        this.importImage("23.jpg"),
        this.importImage("24.jpg"),
        this.importImage("25.jpg"),
        this.importImage("26.jpg"),
        this.importImage("27.jpg"),
        this.importImage("28.jpg"),
        this.importImage("29.jpg"),
        this.importImage("30.jpg"),
        this.importImage("31.jpg"),
        this.importImage("32.jpg"),
        this.importImage("33.jpg"),
        this.importImage("34.jpg"),
        this.importImage("35.jpg"),
        this.importImage("36.jpg"),
        this.importImage("37.jpg"),
        this.importImage("38.jpg"),
        this.importImage("39.jpg"),
        this.importImage("40.jpg"),
        this.importImage("41.jpg"),
        this.importImage("42.jpg"),
        this.importImage("43.jpg"),
        this.importImage("44.jpg"),
        this.importImage("45.jpg"),
        this.importImage("46.jpg"),
        this.importImage("47.jpg"),
        this.importImage("48.jpg"),
        this.importImage("49.jpg"),
        this.importImage("50.jpg"),
      ],
      selectedImage: '',
      selectedImage2: '',
    }
  },
  mounted() {
    this.randomImage()
  },
  methods: {
    importImage(filename) {
      return require(`../assets/images/${filename}`);
    },
    randomImage() {
      const idx = Math.floor(Math.random() * this.image.length)
      const idx2 = Math.floor(Math.random() * this.image.length)
      this.selectedImage = this.image[idx]
      this.selectedImage2 = this.image[idx2]
    }

  },

}
</script>


<style scoped>
.btn{

  background-color: #212529;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  font-size: 30px;
  color: white;
  transition: 0.2s;
  border: none;
  border-radius: 0.7rem;
  box-shadow: 0 0 0.5rem rgba(0, 0, 0, 0.25);
}

.btn:hover {
  background-color: #2e6f76 ;
  color: white ;
}
.image {
  vertical-align: top;
  width: 500px;
  margin: 2px;
  cursor: pointer;
  transition: filter 0.3s ease-in;
}

.image:hover {
  filter: brightness(1.2);
}

</style>
