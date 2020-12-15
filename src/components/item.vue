<template>
<div class="view">
    <input class="toggle" type="checkbox" 
    v-on:click="complete" v-bind:checked="todo.complete">
    <label>{{todo.title}}</label>
    <button class="destroy" v-on:click="remove"></button>
</div>
</template>

<script>
export default {
    name: "item",
    props: {
        todo: Object
    },
    methods: {
        remove() {
            this.$emit('remove', this.todo);
        },
        complete() {
            this.$emit('complete', this.todo);
        }
    }
}
</script>