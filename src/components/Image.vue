<template>
  <div class="hello">
    <div>
      <h1>{{ title }}</h1>
      <h2>{{ msg }}</h2>
    </div>
    <div>
      <button @click="prevImage" class="btn" style="margin-right: 1rem"> {{ '< Prev' }}</button>
      <button @click="nextImage" class="btn" style="margin-left: 1rem">Next ></button>
    </div>
    <div style="margin-top: 1rem">
      <img v-if="image" :key="image.id" @click="nextImage" class="image" :src="image.src" alt="story tell">
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
      image: null,
      images: [
        {
          id: 1,
          src: this.importImage("1.jpg"),
        },
        {
          id: 2,
          src: this.importImage("2.jpg"),
        },
        {
          id: 3,
          src: this.importImage("3.jpg"),
        },
        {
          id: 4,
          src: this.importImage("4.jpg"),
        },
        {
          id: 5,
          src: this.importImage("5.jpg"),
        },
        {
          id: 6,
          src: this.importImage("6.jpg"),
        },
        {
          id: 7,
          src: this.importImage("7.jpg"),
        },
        {
          id: 8,
          src: this.importImage("8.jpg"),
        },
        {
          id: 9,
          src: this.importImage("9.jpg"),
        },
        {
          id: 10,
          src: this.importImage("10.jpg"),
        },
        {
          id: 11,
          src: this.importImage("11.jpg"),
        },
        {
          id: 12,
          src: this.importImage("12.jpg"),
        },
        {
          id: 13,
          src: this.importImage("13.jpg"),
        },
        {
          id: 14,
          src: this.importImage("14.jpg"),
        },
        {
          id: 15,
          src: this.importImage("15.jpg"),
        },
        {
          id: 16,
          src: this.importImage("16.jpg"),
        },
        {
          id: 17,
          src: this.importImage("17.jpg"),
        },
        {
          id: 18,
          src: this.importImage("18.jpg"),
        },
        {
          id: 19,
          src: this.importImage("19.jpg"),
        },
        {
          id: 20,
          src: this.importImage("20.jpg"),
        },
        {
          id: 21,
          src: this.importImage("21.jpg"),
        },
        {
          id: 22,
          src: this.importImage("22.jpg"),
        },
        {
          id: 23,
          src: this.importImage("23.jpg"),
        },
        {
          id: 24,
          src: this.importImage("24.jpg"),
        },
        {
          id: 25,
          src: this.importImage("25.jpg"),
        },
        {
          id: 26,
          src: this.importImage("26.jpg"),
        },
        {
          id: 27,
          src: this.importImage("27.jpg"),
        },
        {
          id: 28,
          src: this.importImage("28.jpg"),
        },
        {
          id: 29,
          src: this.importImage("29.jpg"),
        },
        {
          id: 30,
          src: this.importImage("30.jpg"),
        },
        {
          id: 31,
          src: this.importImage("31.jpg"),
        },
        {
          id: 32,
          src: this.importImage("32.jpg"),
        },
        {
          id: 33,
          src: this.importImage("33.jpg"),
        },
        {
          id: 34,
          src: this.importImage("34.jpg"),
        },
        {
          id: 35,
          src: this.importImage("35.jpg"),
        },
        {
          id: 36,
          src: this.importImage("36.jpg"),
        },
        {
          id: 37,
          src: this.importImage("37.jpg"),
        },
        {
          id: 38,
          src: this.importImage("38.jpg"),
        },
        {
          id: 39,
          src: this.importImage("39.jpg"),
        },
        {
          id: 40,
          src: this.importImage("40.jpg"),
        },
        {
          id: 41,
          src: this.importImage("41.jpg"),
        },
        {
          id: 42,
          src: this.importImage("42.jpg"),
        },
        {
          id: 43,
          src: this.importImage("43.jpg"),
        },
        {
          id: 44,
          src: this.importImage("44.jpg"),
        },
        {
          id: 45,
          src: this.importImage("45.jpg"),
        },
        {
          id: 46,
          src: this.importImage("46.jpg"),
        },
        {
          id: 47,
          src: this.importImage("47.jpg"),
        },
        {
          id: 48,
          src: this.importImage("48.jpg"),
        },
        {
          id: 49,
          src: this.importImage("49.jpg"),
        },
        {
          id: 50,
          src: this.importImage("50.jpg"),
        },
      ]
    }
  },
  mounted() {
    this.nextImage();
  },
  methods: {
    importImage(filename) {
      return require(`../assets/images/${filename}`);
    },
    nextImage() {
      this.image = this.images[this.index];
      this.index = (this.index + 1) % this.images.length;
    },
    prevImage() {
      this.image = this.images[this.index];
      this.index = (this.index - 1) % this.images.length;
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
  width: 800px;
  margin: 2px;
  cursor: pointer;
  transition: filter 0.3s ease-in;
}

.image:hover {
  filter: brightness(1.2);
}

</style>
