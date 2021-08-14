<template>
 <nav class="blue darken-3">
    <div class="nav-wrapper">
      <router-link to="/" class="brand-logo">Tasks</router-link>
      <ul class="right hide-on-med-and-down">
        <router-link             
            to="/"
            custom 
            
            v-slot="{href, navigate, isExactActive }"            
        >
            <li :class="[isExactActive && 'active']"><a :href="href" @click="navigate">Create</a></li>
        </router-link>
        <router-link             
            to="/list"
            custom            
            v-slot="{href, navigate, isActive }"            
        >
            <li :class="[isActive && 'active']"><a :href="href" @click="navigate">List</a></li>
        </router-link>
        
      </ul>
    </div>
  </nav>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
    nav {
      padding: 0 2rem;  
    }
</style>