<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <app-server
                    v-for="server in servers"
                    :server="server">

            </app-server>
        </ul>
    </div>
</template>

<script>
    import { eventBus } from '../../main';
    import Server from './Server.vue';

    export default {
        data: function () {
            return {
                servers: [
                    { id: 1, status: 'Normal'},
                    { id: 2, status: 'Critical'},
                    { id: 3, status: 'Unknown'},
                    { id: 4, status: 'Normal'},
                ],
            };

        },
        components: {
            'app-server': Server,
        },
        methods: {
        }
    }
</script>

<style>

</style>
