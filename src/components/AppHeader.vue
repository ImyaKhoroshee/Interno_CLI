<template>
  <header class="header center">
        <div class="header__logo">
            <svg class="header__icon" width="34" height="34" viewBox="0 0 34 34" fill="none"
                xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M0 34.0003H13.4588V24.499C13.4588 22.4853 15.0898 20.8543 17.1035 20.8543C19.1172 20.8543 20.7482 22.4853 20.7482 24.499V34.0003H33.9975V0C15.2211 0 0 15.2211 0 34.0003Z"
                    fill="#CDA274" />
            </svg>
            <h1 class="header__title"><router-link to="/" class="header__title-link">Interno</router-link></h1>
        </div>
        <nav class="header__navigation">
            <ul class="header__list">
                <li class="header__list-item"><router-link to="/" class="header__link">Home</router-link></li>
                <li class="header__list-item"><router-link to="/project" class="header__link">Project</router-link></li>
                <li class="header__list-item"><router-link to="/blog" class="header__link">Blog</router-link></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
  name: 'AppHeader',
  props: {
    
  }
}
</script>


<style scoped lang="scss">

</style>