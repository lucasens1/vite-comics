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

  img {
    max-width: 100%;
  }
}
</style>