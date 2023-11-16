<template>
    <div>
        <CheckBoxList :items="items">
            <template v-slot:icon="p1">
                <input type="checkbox" :checked="p1.checked"/>
            </template>
            <template v-slot:default="p2">
                <span>{{ p2.label }}</span>
            </template>
        </CheckBoxList>
    </div>
</template>

<script>
import CheckBoxList from './CheckBoxList.vue';

    export default {
    name: "ScopedSlot",
    data() {
        return {
            items: [
                { id: "1", checked: true, label: "hi1" },
                { id: "2", checked: false, label: "hi2" },
                { id: "3", checked: false, label: "hi3" },
                { id: "4", checked: true, label: "hi4" }
            ]
        };
    },
    components: {CheckBoxList }
}
</script>

<style scoped>

</style>