<template>
    <div>
        <h1>{{ special_user }}</h1>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                special_user: ``
            }
        },
        mounted() 
        {
            this.$root.$on(`highlight_username`, this.highlight);
        },
        methods: {
            highlight: function(username)
            {   
                this.special_user = username;
            }
        }
    }
</script>

<style scoped>

</style>