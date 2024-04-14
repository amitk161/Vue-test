<template>
    <div>
        <ChildComp v-on:dateSent='recieveDate' />
        <h1>{{ recievedDate }}</h1>
    </div>
</template>

<script>
import ChildComp from './ChildComp.vue';

export default {
    name: 'ParentComp',
    components: {
        ChildComp
    },
    data() {
        return {
            recievedDate: ''
        }
    },
    methods: {
        recieveDate(date) {
            this.recievedDate = date;
        }
    }
}
</script>