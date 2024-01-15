<script setup>
    import { useSzinhazakStore } from '@/stores/szinhazak';
    const storeSzinhazak = useSzinhazakStore()
</script>

<template>
    <select>
        <option v-for="szinhaz in storeSzinhazak.szinhazak.neve">{{ szinhaz }}</option>
    </select>
    <div>
        <ul>
            <li></li>
        </ul>
        
    </div>

</template>
