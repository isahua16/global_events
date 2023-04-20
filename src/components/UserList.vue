<template>
    <div>
        <section>
            <div v-for="(user, i) in users" :key="i">
                <h3 @click="highlight">{{ users[i] }}</h3>
            </div>
        </section>
    </div>
</template>

<script>
    export default {
        methods: {
            highlight: function(event)
            {
                let username = event[`target`][`innerHTML`];
                this.$root.$emit(`highlight_username`, username);
            }
        },
        data() {
            return {
                users: [`user_1`, `user_2`, `user_3`],
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>