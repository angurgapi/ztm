<template>
	<div class="page-wrapper">
		<div class='shoot'>
			
		  <div class='shoot-header'>
		  	<h2 class='shoot-title' ref='title'>{{ currentShoot.title }}</h2>			
		  </div>
		<p class="shoot-year">year: {{ currentShoot.year }}</p>
		<div class='main-images'>	
		  <img class='cover' :src="`/img/cut/${currentShoot.cover}.webp`">
		  <img class='additional' :src="`/img/sets/${currentShoot.pics[0]}.webp`">
		</div>
		

		<div class='more-pics'>
			<div v-for='pic in currentShoot.pics.slice(1)' class='a-pic'>
	            <img :src="`/img/sets/${pic}.webp`">        
	        </div>
	    </div>
		</div>

</div>
</template>

<style scoped lang='sass'>
.shoot
  padding-top: 100px
  width: 100%
  text-transform: uppercase
  font-family: Courrier New
  .shoot-header
    background: rgba(0,0,0,.9)
    display: flex
    align-items: center
    width: 350px
    height: 85px
    margin: auto
    

    letter-spacing: 3px
  .shoot-title    
    font-size: 32px
    color: #fff
.shoot-year
  color: rgba(0,0,0,.7)
  margin: 20px auto 70px  
  font-weight: 300
  text-align: center
  font-size: 28px
img
  max-width: 900px
.main-images
  display: flex
  flex-direction: row
  justify-content: center
  align-items: center
.cover
  margin-top: 30px
  height: 90vh
.additional
  margin-top: 30px
  height: 70vh

.more-pics
  width: 90%
  margin: 150px auto
  display: flex
  flex-direction: row
  justify-content: center
.a-pic
  display: flex
  justify-content: center

 
    
@media(max-width: 1400px)
  img, .cover
    height: auto
  .main-images, .more-pics, .a-pic
    flex-direction: column
    justify-content: center
  .a.pic
    img
      width: 60vw
      height: auto
  
@media(max-width: 550px)
  img, .additional
    width: 100%
    height: auto
  
</style>
<script>
export default{
  data(){
    return {
        shootList: [
        {title: 'Just Power', cover: 'img1', slug: 'just-power', year: '2019', pics: ['jp-1']},
        {title: 'Teen Power', cover: 'img2', slug: 'teen-power', year: '2019', pics: ['tp-1', 'tp-4']},
        {title: 'Catch Comma', cover: 'img3', slug: 'catch-comma', year: '2020', pics: []},
        {title: 'Research Platform', cover: 'img4', slug: 'research-platform', year: '2019', pics: ['rp-1']},
        {title: 'Fragments', cover: 'img5', slug: 'fragments', year: '2020', pics: []},
        {title: 'Elektroforez', cover: 'img6', slug: 'elektroforez', year: '2018', pics: []},
        {title: 'Ploho', cover: 'img7', slug: 'ploho', year: '2018', pics: []},
        {title: 'Tetiana Chorna', cover: 'img8', slug: 'tetiana-chorna', year: '2019', pics: ['tc-2']},
      ],
      currentShoot: {

      }
    }
  },
  created(){
  	
    for (let shoot of this.shootList){
    	if (shoot.slug == this.$route.params.slug){
    		this.currentShoot = shoot
    		console.log(this.currentShoot)
    	}
    }
  }
}
</script>