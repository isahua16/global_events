<template>
    <div>
        <h4>{{ error_message }}</h4>
        <article v-for="user in all_users" :key="user[`id`]">
            <img :src="user[`avatar`]" alt="">
            <h3>{{user[`first_name`]}} {{user[`last_name`]}}</h3>
            <p>{{user[`email`]}}</p>
        </article>
    </div>
</template>

<script>
import axios from 'axios';
    export default {
        mounted()
        {
            axios.request(
                {
                    url: `https://reqres.in/api/users`
                }
            ).then((response) => {
                let data = response[`data`][`data`];
                this.all_users = data;
            }).catch((error) => {
                error;
                this.error_message = `Something is wrong... Try again.`
            });
        },
        data() {
            return {
                all_users: undefined,
                error_message: undefined
            }
        },
    }
</script>

<style scoped>

</style>