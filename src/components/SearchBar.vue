<template>
    <div>
        <div>
            <select id="music_genre" @change="$emit('SearchGenre', $event.target.value)">
                <option value="All">All</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
            </select>
        </div>

        <div>
            <select id="music_author" @change="$emit('SearchGenre', $event.target.value)">
                <option value="All">All</option>
                <option value="Bon Jovi">Bon Jovi</option>
                <option value="Queen">Queen</option>
                <option value="Sting">Sting</option>
                <option value="Steve Gadd Band">Steve Gadd Band</option>
                <option value="Eric Clapton">Eric Clapton</option>
                <option value="Deep Purple">Deep Purple</option>
                <option value="Metallica">Metallica</option>
                <option value="Dave Weckl">Dave Weckl</option>
                <option value="Michael Jacjson">Michael Jacjson</option>
            </select>
        </div>
    </div>
       
    
  
</template>

<script>
export default {
 name:"SearchBar",

}
</script>

<style>

</style>