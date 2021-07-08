<template>
<div>

    <input type="text" v-model="value.age"/><br/>
    <input type="text" v-model="value.gender"/>
</div>
</template>

<script>
export default {
    name: 'test2',
    props:{
        'value': Object
    },
    watch: {
        value: function(val) {
            this.$emit('change', val);
        }
    }
}
</script>