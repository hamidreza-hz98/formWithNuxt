<template>
    <v-simple-table dark>
        <template v-slot:default>
            <thead>
                <tr>
                    <th class="text-left">
                        Full Name
                    </th>
                    <th class="text-left">
                        Phone Number
                    </th>
                    <th class="text-left">
                        E-mail
                    </th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in tableData" :key="item.name">
                    <td>{{ item.fullName }}</td>
                    <td>{{ item.phoneNumber }}</td>
                    <td>{{ item.email }}</td>
                </tr>
            </tbody>
        </template>
    </v-simple-table>
</template>

<script>
export default {
    data() {
        return {
            props: ['params'],
            tableData: [],

        }
    },

}
</script>