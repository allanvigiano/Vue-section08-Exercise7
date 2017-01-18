<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="! server">Please select a server.</p>
        <div v-else>
            <p>Id: {{server.id}}</p>
            <p>Status: {{server.status}}</p>
        </div>

    </div>

</template>

<script>
    import { eventBus } from '../../main';
    export default {
        data() {
            return {
                    server: null,
            };
        },
        created() {
            eventBus.$on('serverSelected', (server) => {
                this.server = server;
            });

        }
    }
</script>

<style>
</style>
