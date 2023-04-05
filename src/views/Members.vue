<template>
    <div>
        <appHeader title="Members" />
        <template>
            <v-card class="mx-auto" tile>
                <v-list dense>
                    <v-list-item v-for="(item, i) in members" :key="members.id">
                        <v-list-item-avatar rounded="0">
                            <v-img :src="item.img"></v-img>
                        </v-list-item-avatar>

                        <v-list-item-content>
                            <v-list-item-title> <b>{{ item.firstName }} {{ item.middleName ? item.middleName[0] + '.' : ' ' }}
							{{ item.lastName }}</b> </v-list-item-title>
                            <!-- {{item.author.name}} -->
                            <v-list-item-subtitle>{{ item.mobileNo }}</v-list-item-subtitle>
                            <!-- <v-list-item-subtitle>Pages : {{ item.pages }}</v-list-item-subtitle> -->
                        </v-list-item-content>


                        <v-list-item-icon>
                            <div>
                                <v-menu offset-y>
                                    <template v-slot:activator="{ on, attrs }">
                                        <v-btn color="black" dark v-bind="attrs" v-on="on" text>
                                            <v-icon>mdi-dots-vertical</v-icon>
                                        </v-btn>
                                    </template>
                                    <v-list>
                                        <v-list-item>
                                            <v-icon class="mr-2">mdi-pencil</v-icon>
                                            <v-list-item-title>Edit</v-list-item-title>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-icon class="mr-2">mdi-delete</v-icon>
                                            <v-list-item-title>Delete</v-list-item-title>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-icon class="mr-2">mdi-pencil</v-icon>
                                            <v-list-item-title>Issues</v-list-item-title>
                                        </v-list-item>
                                        <v-list-item>
                                            <v-icon class="mr-2">mdi-pencil</v-icon>
                                            <v-list-item-title>Return</v-list-item-title>
                                        </v-list-item>
                                    </v-list>
                                </v-menu>

                                <p>Status</p>
                            </div>
                        </v-list-item-icon>
                    </v-list-item>
                </v-list>

                <v-row align="center" justify="space-around" class="bottom">
                    <v-btn depressed>
                        Previous
                    </v-btn>
                    1
                    <v-btn depressed>
                        Next
                    </v-btn>
                </v-row>
            </v-card>

        </template>
    </div>
</template>

<script>
import membersList from "@/data/members.json";
import appHeader from "@/components/appHeader.vue";
export default {
    data() {
        return {
            members: membersList
        }
    },
    components: {
        appHeader,
    },
}
</script>

<style lang="scss" scoped>
.bottom{
    // margin-bottom:10px;
    padding: 20px;
    padding-top: 0px;
}
</style>