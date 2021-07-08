<template>
<div>

    <input type="text" v-model="value.name"/><br/>
    <input type="text" v-model="value.address.brgy"/>
    <input type="text" v-model="value.address.town"/>
    <input type="text" v-model="value.address.city"/>
</div>
</template>

<script>
export default {
    name: 'test',
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