<template>
  <div class="container">
    <div class="mosaic">
      <div v-for='item in shootList' class='shoot'>
        <img :src="`/img/cut/${item.cover}.webp`" @click='card(item.slug)'>
        <h2 class='shoot-name'>{{ item.title }}</h2>
      </div>
    </div>
  </div>
</template>

<style lang='sass'>
.container
  margin: 0 auto
  min-height: 100vh
  display: flex
  justify-content: center
  align-items: center
  text-align: center

.mosaic
  display: grid
  grid-template-columns: repeat(4, 25%)
  grid-template-rows: repeat(2, 50%)
  gap: 0
  margin: 100px auto 100px auto
  width: 50%
  .shoot-name
    font-family: Courier New
    text-transform: uppercase
    position:  absolute
    z-index: 1001
    top: 100px
    font-size: 1rem
    max-width: 100%
    word-wrap: break-word
  img
    height: 100%
    width: 100%
    opacity: .6
  
  img:hover
    opacity: .9
  .shoot:nth-child(odd)
    -webkit-animation: rotation 16s infinite ease-in-out

  .shoot:nth-child(even)
    -webkit-animation: rotation 12s infinite ease-in-out

@-webkit-keyframes rotation
  from 
    -webkit-transform: rotate(0deg)
    
  to
    -webkit-transform: rotate(359deg)
  
@media(max-width: 500px)
  .mosaic
    max-width: 55%
    grid-template-columns: repeat(2, 50%)
    grid-template-rows: repeat(4, 25%)

</style>

<script>
export default {
  data(){
    return {
      shootList: [
        {title: 'Just Power', cover: 'img1', slug: 'just-power'},
        {title: 'Teen Power', cover: 'img2', slug: 'teen-power'},
        {title: 'Catch Comma', cover: 'img3', slug: 'catch-comma'},
        {title: 'Research Platform', cover: 'img4', slug: 'research-platform'},
        {title: 'Fragments', cover: 'img5', slug: 'fragments'},
        {title: 'Elektroforez', cover: 'img6', slug: 'elektroforez'},
        {title: 'Ploho', cover: 'img7', slug: 'ploho'},
        {title: 'Tetiana Chorna', cover: 'img8', slug: 'tetiana-chorna'},
      ]
    }
  },
  methods: {
    card(slug){
      this.$router.push(`/shoots/${slug}`)
    }
},
}
</script>
