<template>
  <div class="v-table">
        <v-table-main-row 
          :attributes="attributes"
          :style="{ gridTemplateColumns: count_columns }"  
        />
        <v-table-row
          :style="{ gridTemplateColumns: count_columns }"
          :attributes="attributes"
          v-for="(record, index) in records" 
          :key="index" 
          :record="records[index]"
        />
  </div>
</template>

<script>
import vTableMainRow from './v-table-main-row'
import vTableRow from './v-table-row'

export default {
    name: 'v-table',
    components: {
        vTableMainRow,
        vTableRow
    },
    computed: {
        count_columns() {
            return 'repeat(' + this.attributes.length + ', 110px)'
        },
    },
    data() {
        return {
            attributes: [
                {
                    'attribute': 'subject',
                    'type': 'string'
                },
                {
                    'attribute': 'teacher',
                    'type': 'string'    
                },
                {
                    'attribute': 'reporting',
                    'type': 'string'
                }
            ],
            records: [
                {
                    'subject' : 'Probability theory',
                    'teacher': 'Tyurneva Tatyana Gennadyevna',
                    'reporting': 'Exam'
                },
                {
                    'subject' : 'Data Mining',
                    'teacher': 'Kazimirov Alexander Sergeevich',
                    'reporting': 'Exam'
                },
                {
                    'subject' : 'Information Security',
                    'teacher': 'Mutsenyuk Vitus Evgenievich',
                    'reporting': 'Exam'
                },
                {
                    'subject' : 'Numerical analysis',
                    'teacher': 'Antonik Vladimir Georgievich',
                    'reporting': 'Exam'
                },
            ]
        }
    },
    methods: {

    },
    mounted() {
        // console.log('v-table')
        // console.log(this.records)
        // console.log(this.records.length)
    }

}
</script>

<style>
    .v-table {
        margin: auto;
        display: grid;
        grid-template-columns: 1fr;
        grid-row-gap: 5px;
        font-family: Raleway;
    }
</style>