<template>
	<div class="page-wrapper">

		<div class="background">
		  <div class="bg-left"></div>
		  <div class="bg-right"></div>				
		</div>	
			
		<div class="text-wrapper">
		  <div class='intro-text'>
			<p><strike><i>ZTM BUREAU</i></strike> IS AN ART AGENCY THAT WORKS ON YOUR VISUAL REPRESENTATION IN BOTH THE DIGITAL AND THE ANALOG WORLD.
			<br>THE BUREAU WAS BORN FROM A COLLABORATION OF TWO ARTISTS: ZULEIKHA MURTAZAIEVA AND TANIA SUSLIK. THEY MET IN JANUARY 2019, A SOMBER HARMONY OF WINTER KYIV HOLDS TOGETHER THEIR AESTHETIC PERSPECTIVE AND PERFORMANCE PRINCIPLE.
			<br>FOR THE TIME BEING, THE BUREAU FOCUSES ON BLACK AND WHITE TO PORTRAY PEOPLE, OBJECTS AND PHENOMENA. BUT COLOUR IS COMING SOON.</p>
			<a class='link' href="#section-a">works</a>
			<p class='contact-us'>FEEL FREE TO CONTACT US AND SHAPE YOUR IDEAS IN STORIES AND IMAGES TOGETHER.</p>
			<a class='link email' href="mailto:talktoztm@protonmail.com">talktoztm@protonmail.com</a>
		  </div>
		</div>
	</div>
</template>

<style scoped lang='sass'>

.background
  display: flex
  flex-direction: row
  width: 80vw
  max-width: 650px
  height: 80vh
  max-height: 500px
  position: relative
  top: 20vh

.bg-left
  position: relative
  background-image: url('/img/paper.webp')
  width: 50%
  background-size: cover

.text-wrapper
  display: flex
  justify-content: center
  align-items: center
  position: absolute
  top: 30vh
.intro-text
  width: 70vw
  max-width: 600px
  font-family: Courier New
  font-weight: 400
  z-index: 1001
  line-height: 16px
  white-space: pre-wrap
  text-align: justify

.contact-us
  width: 65%

.link
  color: rgb(47,96,7)
  float: right
  text-transform: uppercase
  font-size: 16px
  text-decoration: none
  border-bottom: 1px solid rgb(47,96,7)

.email
  float: left
@media(max-width: 500px)
  .background
    width: 100vw
  .intro-text
    width: 90vw
</style>