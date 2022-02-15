<template>
	<input :value="modelValue" @input="updateInput" class="input" type="text">
</template>

<script>
    export default {
        name: 'form-input',
		    props: {
            modelValue: [String, Number]
		    },
		    methods: {
            updateInput(event){
                this.$emit('update:modelValue', event.target.value)
		            console.log(event.target.value)
            }
		    }

    }
</script>

<style scoped>
	.input {
		margin-bottom: 15px;
		width: 100%;
		height: 35px;
		border: 1px solid turquoise;
	}
</style>