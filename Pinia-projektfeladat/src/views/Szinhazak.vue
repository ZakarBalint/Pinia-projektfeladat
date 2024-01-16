<script setup>
    import { useSzinhazakStore } from '@/stores/szinhazak';
    const storeSzinhazak = useSzinhazakStore();
</script>

<template>
    <select @change="storeSzinhazak.onChange($event)">
        <option></option>
        <option v-for="szinhaz in storeSzinhazak.szinhazak">{{ szinhaz.neve }}</option>
    </select>
    <div>
        <ul>
            <li v-for="eloadasok in storeSzinhazak.selectedEloadasok"><a href="{{ eloadasok.url }}">{{ eloadasok.cim }}</a></li>
        </ul>        
    </div>

</template>
