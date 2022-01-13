<template>
    <label class="radio-item"><slot /><input type="radio" @click="$parent.$options.name === 'RadioGroup' ? $parent.$emit('update:modelValue', value) : $emit('update:modelValue', value)" :disabled="_disabled" :checked="checked" /></label>
</template>

<script>
export default {
    props: {
        value: {
            required: true
        },
        disabled: {
            type: Boolean,
            default: false
        },
        'model-value': null
    },
    computed: {
        _disabled () {
            return this.disabled || this.$parent.$props.disabled
        },
        checked () {
            return (this.$props.modelValue || this.$parent.$props.modelValue) === this.value
        }
    },
    mounted () {
        console.log(this.$parent.$props.modelValue)
    }
}
</script>