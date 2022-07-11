<template>
    <div>
    <select id="music_genre" @change="$emit('SearchGenre', $event.target.value)" value="0">
        <option value="All">All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
  </select>
    </div>
  
</template>

<script>
export default {
 name:"SearchBar",

}
</script>

<style>

</style>