<template>
    <label :class="getClassForFieldInput(schema)">
        <input
            type="checkbox"
            v-model="value"
            :autocomplete="schema.autocomplete"
            :disabled="disabled"
            :name="schema.inputName" >
        <span class="label-body">{{ schema.label }}</span>
</template>

<script>
    import VueFormGenerator from "../../src";

    export default {
        mixins: [ VueFormGenerator.abstractField ]
    };
</script>

<style lang="sass">
    .vue-form-generator .field-checkbox input {
        margin-left: 12px;
    }
</style>