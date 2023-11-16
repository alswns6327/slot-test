<template>
    <div v-for="item in items" :key="item.id">
        <slot name="icon" :checked="item.checked"></slot>
        <slot :label="item.label"></slot>
    </div>
</template>
<script>
export default{
    name : "CheckBoxList",
    props : ["items"],
    created(){
        console.log(this.items.length);
    }
}
</script>