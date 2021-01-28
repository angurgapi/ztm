<template>
<nav role="navigation" aria-label="main navigation">      
    <div class="navbar">
        <nuxt-link to="/" class="navbar-item is-half">
            ztm
        </nuxt-link>
        
        <nuxt-link
            active-class="is-active"
            to="/about"
            class="navbar-item"
            exact
          >About & contact</nuxt-link>      
      </div>
    </nav>
</template>

<script>
	export default{

	}
</script>

<style scoped lang='sass'>
nav
  background-color: #fff
  position: fixed
  z-index: 1002
  width: 100%
  box-shadow: 0 4px 6px -2px rgba(0,0,0,.3)
.navbar
  height: 70px
  width: 100%
  display: flex
  justify-content: center
  align-items: center  
  flex-direction: row
  padding-left: 0
  a
    text-decoration: none
    font-family: Courier New
    text-transform: uppercase
    letter-spacing: 3px
    color: rgba(0,0,0,.7)
    font-size: 22px
    font-weight: 300
    margin-right: 20px
  .nuxt-link-exact-active
    color: rgba(0,0,0,.5)  
.nuxt-link, .nuxt-link-active
  text-decoration: none
  color: rgba(0,0,0,.8)  
</style>