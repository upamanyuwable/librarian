<template>
    <div class="center">
        <!-- ek page me 12 columns hoteh hume login form k liye 10 chahiye isliye left aur right m ek column chodenge -->
        <v-row>
            <v-col cols="10" offset="1" sm="6" offset-sm="3" md="8" offset-md="2">
                <v-avatar color="surface-variant" rounded="0" size="60">
                <v-img src="@/assets/logo.png"></v-img>
            </v-avatar>
            <v-text-field label="UserName" v-model="username"></v-text-field>
            <v-text-field label="password" type="password" v-model="password"></v-text-field>
            <v-btn block @click="authenticate" class="base-inverted">
                Click
            </v-btn>
            </v-col>
        </v-row>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                username: "",
                password: ""
            }
        },
        methods: {
            authenticate() {
                alert("User Created");
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>