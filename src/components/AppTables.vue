<template>
    <div :class="styles">
        <h3>{{tittle}}</h3>
        <p>{{description}}</p>
        <table>
            <thead>
                    <tr>
                        <th>Nombre</th>
                        <th>Apellido</th>
                        <th>Organización</th>
                        <th>Llegada</th>
                    </tr>
            </thead>
            <tbody>
                <tr v-for="(participant, i) in participants" :key="i">
                    <th v-for="(row, r) in participant" :key="r">{{row}}</th>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    name: 'AppTables',
    props: {
        tittle: {
            type: String,
            required: true,
        },
        description: {
            type: String,
            required: true,
        },
        participants: {
            type: Array,
            required: true,
        },
        styles: {
            type: String,
            required: true,
        },
    },    
}
</script>

<style scoped>

    p {
        font-size: 16px;
    }

    table {
        margin: 5px;
        padding: 5px;
    }

    thead tr th {
        font-size: 14px;
        font-weight: bold;
        padding: 5px;
    }

    tbody tr th {
        font-size: 14px;
        font-weight: normal;
        padding: 5px;
    }

    .day-one h3 {
        color: rgb(98, 2, 193);
        font-size: 18px;
        margin-top: 35px;
    }

    .day-one table {
        background-color: rgba(98, 2, 193, 0.15);
    }

    .day-one thead tr th {
        color: rgb(98, 2, 193);
    } 

    .day-two h3 {
        color: rgb(42, 99, 156);
        font-size: 18px;
        margin-top: 35px;
    }

    .day-two table {
        background-color: rgba(42, 99, 156, 0.15);
    }

    .day-two thead tr th {
        color: rgb(42, 99, 156);
    } 

    .day-three h3 {
        color: rgb(0, 171, 123);
        font-size: 18px;
        margin-top: 35px;
    }

    .day-three table {
        background-color: rgba(0, 171, 123, 0.15);
    }

    .day-three thead tr th {
        color: rgb(0, 171, 123);
    } 

</style>