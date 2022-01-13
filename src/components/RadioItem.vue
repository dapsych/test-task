<template>
    <label class="radio-item"><slot /><input type="radio" @click="$parent.$emit('update:modelValue', value)" :disabled="disabled" :checked="checked" /></label>
</template>

<script>
export default {
    props: {
        value: {
            required: true
        }
    },
    computed: {
        disabled () {
            return this.$parent.$props.disabled
        },
        checked () {
            return this.$parent.$props.modelValue === this.value
        }
    }
}
</script>