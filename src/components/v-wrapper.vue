<template>
    <div class="v-wrapper">
        <v-table />
    </div>
</template>

<script>
import vTable from './v-table'

export default {
    name: 'v-wrapper',
    components: {
        vTable,
    }

}
</script>

<style>
    .v-wrapper {
        margin: auto;
        width: 1020px;
        padding: 10px;
        border-radius: 2px;
        min-height: 800px;
        background-color: rgba(94, 129, 255, 0.5);
    }
</style>