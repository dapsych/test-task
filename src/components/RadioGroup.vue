<template>
    <div class="radio-group">
        <slot></slot>
    </div>
</template>

<script>
export default {
    name: 'RadioGroup',
    props: {
        disabled: {
            type: Boolean,
            default: false
        },
        'model-value': null
    }
}
</script>

<style scoped>
    .radio-group {
        display: flex;
        flex-direction: column;
    }
</style>