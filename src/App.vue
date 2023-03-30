<template>
  <header>
    <NavBar />
    <main class="Intro-section">
      <img src="../src/images/Vue_logo.png" />
      <h1>Welcome to Vue.js</h1>
      <h3>Become a coding ninja with the fastest-growing JavaScript framework</h3>
      <button src="../src/images/Buttton shape.png">Awesome!</button>
    </main>
    <section class="greenZone">
      <Targets v-for="Targets in greenZone" :key="Targets.id"
        :icon="Targets.icon"
        :title="Targets.title"
        :description="Targets.description"
      />
    </section>
  </header>
</template>

<script >
import NavBar from './components/NavBar.vue';
import Targets from './components/Targets.vue';
export default {
  name: 'App',
  components: {
    NavBar,
    Targets
},
  data(){
    return {
      target: [{
        icon:'../images/USP-1.svg',
        title:'Performant',
        description:'Truly reactive, compiler-optimized rendering system that rarely requires manual optimization.',
      }
      ,{
        icon:'../images/USP-2.svg',
        title:'Approachable',
        description:'Builds on top of standard HTML, CSS and JavaScript with intuitive API and world-class documentation.',
      },
      {
        icon:'../images/USP-3.svg',
        title:'Versatile',
        description:'A rich, incrementally adoptable ecosystem that scales between a library and a full-featured framework.',
      }
      ]
    }
  }
}
</script>

<style scoped>
@import url(https://fonts.google.com/share?selection.family=Inter:wght@400;800);

*{
  font-family: Inter;
}
.Intro-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 299px;
}

.Intro-section img {
  margin-top: 37px;
  width: 128px;
  height: 129px;
}

.Intro-section h1 {
  margin-top: -30px;
  color: #2b2f30;
  font-size: 50px;
  font-family: Inter;
  font-weight: 800;
  line-height: 95px;
  letter-spacing: -0.02em;
  text-align: center;
}

.Intro-section h3 {
  max-width: 309px;
  margin-top: -40px;
  color: black;
  font-family: Inter;
  font-size: 14px;
  font-weight: 800;
  font-style: Bold;
  line-height: 20px;
  letter-spacing: -2%;
  text-align: center;
}

.Intro-section button {
  color: white;
  width: 121px;
  height: 31px;
  border-radius: 13px;
  background-color: #34495e;
}

.greenZone{
  display: flex;
  justify-content: space-between;

}
</style>
