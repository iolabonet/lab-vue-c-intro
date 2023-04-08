<template>
  <div id="greenZone">
    <Targets
      v-for="item in items"
      :key="item.id"
      :icon="'./images/USP-' + item.id"
      :title="item.title"
      :description="item.description"
    />
  </div>
</template>

<script>
import Targets from './Targets.vue'
export default {
  components: {
    Targets
  },
  data() {
    return {
      items: [
        {
          icon: '1.png',
          title: 'Performant',
          description:
            'Truly reactive, compiler-optimized rendering system that rarely requires manual optimization.'
        },
        {
          icon: '2.png',
          title: 'Approachable',
          description:
            'Builds on top of standard HTML, CSS and JavaScript with intuitive API and world-class documentation.'
        },
        {
          icon: '3.png',
          title: 'Versatile',
          description:
            'A rich, incrementally adoptable ecosystem that scales between a library and a full-featured framework.'
        },
      ]
    }
  }
}
</script>

<style scoped>
#greenZone {
  background-color: #39b983;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 2em 2em;
  margin: 2em auto;
}

div {
    text-align: center;
}
</style>