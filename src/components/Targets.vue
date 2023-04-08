<template>
  <div>
    <img :src="icon"/>
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: 'Targets',
  props: {
    icon: {
      type: String
    },
    title: {
      type: String
    },
    description: {
      type: String
    }
  }
}
</script>


<style scoped>
div {
  text-align: center;
  width: 125px;
}

img {
  width: 60px;
  height: 60px;
  margin-bottom: 30px;
}

h2,
p {
  font-style: normal;
  letter-spacing: -0.02em;
  text-align: center;
}

h2 {
  font-weight: bold;
  font-size: 1em;
  margin: 5px 0;
}

p {
  font-size: 12px;
  line-height: 17px;
  letter-spacing: -0.02em;
  text-align: center;
}
</style>