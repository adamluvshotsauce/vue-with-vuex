<template>
    <div>
        <button class="btn btn-primary" @click="increment(100)">Increment</button>
        <button class="btn btn-primary" @click="decrement(50)">Decrement</button>
    </div>
</template>

<script>
    import * as types from '../store/types';
    import { mapActions } from 'vuex';

    export default {
        methods: {
            ...mapActions({
                increment: types.COUNTER_INCREMENT,
                decrement: types.COUNTER_DECREMENT
            })
        }
    }
</script>