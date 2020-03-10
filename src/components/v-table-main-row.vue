<template>
    <div class="v-table-main-row">
        <v-table-cel-of-row 
            class="header-cel" 
            v-for="attr in attributes"
            :key="attr.attribute" 
            :content="attr.attribute"
        />
    </div>
</template>

<script>
    import vTableCelOfRow from './v-table-cel-of-row'

    export default {
        name: 'v-table-main-row',
        components: {
            vTableCelOfRow,
        },
        props: ['attributes'],
    }
</script>

<style>
    .v-table-main-row {
        display: grid;
        gap: 5px;
    }
</style>