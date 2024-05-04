<script>
export default{
    props : {
        img : String,
        name : String,
        altext : String
    }
};
</script>

<template>
    <div class="card">
        <img :src="img" :alt="altext" />
        <h6>{{ name }}</h6>
      </div>
</template>

<style lang="scss" scoped>
.card {
  background-color: white;
  padding: 1rem;
  text-align: center;
  border: 3px solid black;
  height : 100%;
  img {
    max-width: 100%;
    height: 80%;
  }
  h6 {
    margin-top : 1rem;
  }
}
</style>