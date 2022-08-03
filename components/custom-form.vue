<template>
    <v-form v-model="valid" @submit.prevent="handleSubmit">
        <v-container>
            <v-row>
                <v-col cols="6">
                    <v-col cols="12" md="4">
                        <v-text-field v-model="firstName" :rules="nameRules" label="First name" required>
                        </v-text-field>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-text-field v-model="lastName" label="Last name">
                        </v-text-field>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-text-field v-model="phoneNumber" :rules="phoneRules" label="Phone number">
                        </v-text-field>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-text-field v-model="email" :rules="emailRules" label="E-mail"></v-text-field>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-btn block type="submit" color="primary" elevation="2" large outlined rounded>Submit
                        </v-btn>
                    </v-col>
                </v-col>
                <v-col cols="6">
                    <custom-form />
                </v-col>

            </v-row>

        </v-container>
    </v-form>
</template>

<script>
export default {
    data() {
        return {
            valid: false,
            firstName: '',
            lastName: '',
            nameRules: [
                v => !!v || 'First name is required',
            ],
            phoneNumber: '',
            phoneRules: [
                v => v.length >= 8 || 'Phone number should be more than 8 characters'
            ],
            email: '',
            emailRules: [
                v => /.+@.+/.test(v) || 'E-mail must be valid',
            ],

        }
    },
    methods: {
        handleSubmit(event) {
            event.preventDefault();
        }
    }
}
</script>

