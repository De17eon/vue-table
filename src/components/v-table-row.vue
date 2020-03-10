<template>
    <div class="v-table-row">
        <v-table-cel-of-row 
          v-for="(value, index) in record" 
          :key="index" 
          :content="value" 
        />
    </div>
</template>

<script>
    import vTableCelOfRow from './v-table-cel-of-row'

    export default {
        name: 'v-table-row',
        components: {
            vTableCelOfRow
        },
        props: ['attributes', 'record'],
        methods: {
            check() {
                var attrs = this.$props.attributes;
                var record = this.$props.record;

                var i = 0;
                var e = false; // e - error
                for (var prop in record) {
                    console.log(attrs[i].attribute, '=?=', prop)
                    if (attrs[i].attribute != prop) {
                        e = true;
                        break;    
                    }
                    i++; 
                }
                if (e == true){
                    return 'В строке есть ошибка!'
                }
                return 'Строка правильная'
            }
        },
        mounted() {
            console.log('v-table-row: ')
            // console.log(this.$props.record)
            // console.log(this.$props.attributes)
            console.log(this.check())
        }
    }
</script>

<style>
    .v-table-row {
        display: grid;
        grid-column-gap: 5px;
    }
    .cel {
        background-color: rgb(160, 166, 211);
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>