<template>
    <div>
        <v-row class="appHeader">
            <v-col col="10">
                <h2>{{ title }}</h2>
            </v-col>
            <div class="v-right">
                <v-col col="2">
                    <v-btn small text @click="$emit('add')"> 
                        <v-icon>mdi-plus</v-icon>
                    </v-btn>
                </v-col>
            </div>
        </v-row>
        <v-row>
            <v-col>
                <v-text-field outlined label="Search" append-icon="mdi-magnify" @input="$emit('search',$event) " placeholder="Search"></v-text-field>
            </v-col>
        </v-row>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
        },
    },
}
</script>

<style lang="scss" scoped>
.appHeader {
    padding: 1rem;
}
</style>