<template>
  <div class="jumbotron" :style="'background-image:' + backgroundImage(slider[index].image)">
    <div class="overlay">
      <h2 class="title">{{slider[index].title}}</h2>
      <p class="sub-title">{{slider[index].subTitle}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Jumbotron',
  data(){
    return {
      index: 0,
      slider: [
        {
          image: 'jumbotron.jpg',
          title: 'Testo prova Jumbotron',
          subTitle: 'Sub titolo prova Jumbotron'
        }
      ]
    }
  },
  methods:{
    backgroundImage: function(path){
      return `url(${require(`@/assets/img/${path}`)})`;
    }
  }

}
</script>

<style scoped lang="scss">
.jumbotron{
  width: 100%;
  height: 320px;
  overflow: hidden;
  background-size: cover;

  img{
    width: 100%;
  }
}

.overlay{
  background: rgba(0,0,0, 0.5);
  height: 100%;
  padding: 150px 263px 0;
}

.title{
  color: white;
  font-size: 2rem;
  text-transform: uppercase;
  font-weight: 700;
}

.sub-title{
  color: white;
  font-size: 1.5rem
}
</style>