<script setup>
    import { useSzinhazakStore } from '@/stores/szinhazak';
    const storeSzinhazak = useSzinhazakStore()
</script>

<template>
    <select>
        <option v-for="szinhaz in storeSzinhazak.szinhazak" @click="storeSzinhazak.setselectedEloadasok()">{{ szinhaz.neve }}</option>
    </select>
    <div>
        <ul>
            <li v-for="eloadasok in storeSzinhazak.selectedEloadasok"><a href={{ eloadasok.url }}>{{ eloadasok.neve }}</a></li>
        </ul>        
    </div>

</template>
