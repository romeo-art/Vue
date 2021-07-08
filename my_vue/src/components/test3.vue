<template>
<div>

    <input type="text" v-model="value.status"/><br/>
    <input type="text" v-model="value.school"/>
</div>
</template>

<script>
export default {
    name: 'test3',
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