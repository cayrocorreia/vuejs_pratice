<template>
    <v-container fluid>
        <div class="pills">
            <Pill v-for="word in groupWords" :key="word.name" 
            :name="word.name" :amount="word.amount"  />

        </div>
    </v-container>  
</template>

<script>
import Pill from './Pill'

export default {
    components: { Pill },

    data: function () {
        return {
            groupWords: [
                { name: 'i', amount: 1234 },
                { name: 'you', amount: 400 },
                { name: 'he', amount: 555 },
            ]
        }

    }
 
}
</script>

<style>
.pills{
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}

</style>