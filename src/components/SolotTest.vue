<template>
    <div>
        <h3>기술</h3>
        <CheckBox2 v-for="item in items" :key="item.id" :id="item.id"
            :checked="item.checked" @check-changed="CheckBoxChanged">
            <span v-if="item.checked" style="color : blue;text-decoration: underline;">
                <i>{{ item.label }}</i>
            </span>
            <span v-else style="color:gray;">{{ item.label }}</span>
        </CheckBox2>
    </div>
</template>
<script>
import CheckBox2 from './CheckBox2.vue';

export default {
    name: "SlotTest",
    components: { CheckBox2 },
    data(){
        return {
            items : [
                {id : 1, checked : true, label : "1212"},
                {id : 2, checked : false, label : "1213"},
                {id : 3, checked : false, label : "1214"},
                {id : 4, checked : true, label : "1215"},
                {id : 5, checked : false, label : "1216"},
            ]
        }
    }
}
</script>