<template>
    <div class="controls">
        <input type="button" value="Increment" @click="increment">
        <input type="button" value="Decrement" @click="decrement">
    </div>
</template>

<script>
import { mapActions } from 'vuex'
export default {
    name: 'controls',
    methods: mapActions([
        'increment',
        'decrement'
    ])

}
</script>

<style>

</style>