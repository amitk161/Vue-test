<template>
    <div>
        <button v-on:click="notifyParent">Click Me!</button>
    </div>
</template>

<script>
export default {
    name: 'ChildComp',
    methods: {
        notifyParent() {
            let currentDate = new Date();
            this.$emit('dateSent', currentDate);
        }
    }
}
</script>