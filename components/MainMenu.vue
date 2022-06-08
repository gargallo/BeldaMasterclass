<template>
  <nav>
    <ul>
      <li v-for="item in menu" :key="item.url">
        <nuxt-link :to="item.url">
          {{ item.name }}
        </nuxt-link>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'MainMenu',
  data () {
    return {
      menu: [
        {
          name: 'Home',
          url: '/'
        },
        {
          name: 'About',
          url: '/about'
        },
        {
          name: 'Products',
          url: '/products'
        }
      ]
    }
  }
}
</script>
