<template>
  <div class="wrapper">
    <div class="resorts">
      <div class="resort" v-for="resort in resorts" :key="resort.id">
        <div
          class="info"
          :style="
            'background: linear-gradient(rgba(0, 0, 0, 0.45), rgba(0, 0, 0, 0.45)), url(\'/images/' +
            resort.image +
            '\')'
          "
        >
          <router-link :to="'/resorts/' + resort.id">
            <h1>{{ resort.name }}</h1>
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ResortList",
  props: {
    resorts: Array,
  },
};
</script>

<style scoped>
a:-webkit-any-link {
  color: white;
}

a:-webkit-any-link:hover {
  color: rgb(243, 135, 149);
}

.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: "Times New Roman", Times, serif;
}

.resorts {
  width: 100%;
  margin-top: 5em;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.resort {
  width: 90%;
  height: 35em;
  display: flex;
}

.resort img {
  border: 2px solid #333;
  object-fit: cover;
}

.resort .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.info {
  background-repeat: no-repeat;
  color: rgb(255, 255, 255);
  flex: 1;
  padding: 10px 30px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.info h1 {
  font-size: 60px;
}

.info h2 {
  font-size: 14px;
}

.info p {
  margin: 0px;
  font-size: 10px;
}

.price {
  display: flex;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
}
</style>
