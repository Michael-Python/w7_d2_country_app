<template lang="html">
  <div id="favourite_countries">
    <h2>Favourite Countries</h2>
    <ul>
      <li v-for="(country, index) in favouriteCountries" v-bind:key="index">
        <span id="country-name">English Name: {{country.name}}</span>
        <br>
        <span id="country-name">Native Name: {{country.nativeName}}</span>
        <br>
        <span id="country-pop">Population: {{country.population}}</span>
        <br>
        <img width=50% class="lrg-flag" :src="country.flag"/>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'favourite-countries',
  props: ['favouriteCountries']
}
</script>

<style lang="css" scoped>
</style>

<style>
ul {
  display: flex;
  flex-wrap: no wrap;
  justify-content: center;
}
#country-name {
  font-size: 15px;
}



</style>
