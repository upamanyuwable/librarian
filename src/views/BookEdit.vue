<template>
    <div>
        <h1>{{id != 0 ? "Edit":"Add"}} book</h1>
        <v-form>
            <v-text-field label="Title" v-model="book.title"> </v-text-field>
            <v-text-field label="Description" v-model="book.description"> </v-text-field>
        </v-form>
        {{ book }}
    </div>
</template>

<script>
import booksList from '@/data/books.json'
    export default {
        data(){
            return{
                id:0,
                book:""
            }
        },
        mounted(){
            this.id= this.$route.params.id;
            console.log(this.id);   
            if(this.id!=0){
                this.book=booksList.find(x => x._id == this.id)
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>