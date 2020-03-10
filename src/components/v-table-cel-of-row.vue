<template>
    <div class="v-table-cel-of-row">{{ content }}</div>
</template>

<script>
export default {
    name: 'v-table-cel-of-row',
    props: ['content'],
    mounted() {
        // console.log('v-table-cel-of-row')
        // console.log(this.$props.content)
    }
}
</script>

<style>
    .v-table-cel-of-row {
        background-color: #5E81FF;
        display: flex;
        align-items: center;
        justify-content: left;
        text-align: left;
        border: 2px solid #914AE8;
        border-radius: 2px;
        padding: 3px;
        color: whitesmoke;
    }

    .header-cel {
        background-color: #914AE8;
        color: whitesmoke;
    }

    .v-table-cel-of-row:hover {
        background-color: rgba(145, 74, 232, 0.733);
        transition: 300ms ease;
    }

    /* .header-cel:hover {
        background-color: #FF4DD7;
    } */

    
    .table-1-hex { color: #A61B34; }
    .table-2-hex { color: #C1C9D9; }
    .table-3-hex { color: #8694A6; }
    .table-4-hex { color: #254559; }
    .table-5-hex { color: #A63737; }

    /* Color Theme Swatches in RGBA
    .table-1-rgba { color: rgba(165, 26, 52, 1); }
    .table-2-rgba { color: rgba(193, 200, 216, 1); }
    .table-3-rgba { color: rgba(133, 147, 165, 1); }
    .table-4-rgba { color: rgba(36, 68, 89, 1); }
    .table-5-rgba { color: rgba(165, 54, 54, 1); } */

    /* Color Theme Swatches in HSLA 
    .table-1-hsla { color: hsla(349, 72, 37, 1); }
    .table-2-hsla { color: hsla(220, 23, 80, 1); }
    .table-3-hsla { color: hsla(213, 15, 58, 1); }
    .table-4-hsla { color: hsla(203, 41, 24, 1); }
    .table-5-hsla { color: hsla(0, 50, 43, 1); } */
</style>