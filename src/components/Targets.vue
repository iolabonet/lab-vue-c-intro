<template>
    <img :src="icon" alt="icon of targets">
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
</template>

<script>
export default {
    name: 'Targets',
    props: {
        icon: {
            type: String,
        }
        title: {
            type: String,
        }
        description: {
            type: String,
        }
       }
    }

</script>


<style scoped>
img {
  width: 60px;
  height: 60px;
  margin-bottom: 30px;
}
h2, p {
  font-family: Inter;
  font-style: normal;
  letter-spacing: -0.02em;
  text-align: center;
}
h2 {
  font-weight: 700;
  font-size: 16px;
  margin-bottom: 30px;
}
p {
  font-weight: 400;
  font-size: 12px;
  line-height: 17px;
  letter-spacing: -0.02em;
  text-align: center;
}
</style>