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
            tableData: [
                {
                    fullName: 'Hamidreza Hassnazadeh',
                    phoneNumber: '09153456486',
                    email: 'hamidreza@matican.com'
                },
                {
                    fullName: 'Ali Azimi',
                    phoneNumber: '09155386486',
                    email: 'ali@matican.com'
                },
                {
                    fullName: 'Daniel Azimi',
                    phoneNumber: '09155562486',
                    email: 'Daniel@matican.com'
                },
                {
                    fullName: 'Adriana Nahaani',
                    phoneNumber: '0915347778',
                    email: 'Adriana@matican.com'
                },

            ],
        }
    },
}
</script>