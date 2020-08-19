<template>
    <div>
        <div id="example-1">
            <button @click="upFunction" class="btn btn-info">{{ lable }}</button>
            <button @click="downFunction" class="btn btn-info ml-3">{{ 0 }}</button>
            <p v-bind:style="{ fontSize: fsize + 'px' }">HELLO {{counter}}</p>
        </div>
    </div>
</template>
<script>
export default {
    data: function() {
        return {
            counter: 0,
            fsize:20
        }
    },
    props: {
        lable: String,
    },
    methods: {
        upFunction: function() {
            this.counter += 1
            this.fsize += 10

            //console.log(this.fsize);
            //console.log(this.counter);

            //ส่งค่าตัวแปร counter ออกไปโดยผ่านตัวแปร cc
            this.$emit('cc', this.counter)
        },
        downFunction: function() {
            this.counter -= 1
            this.fsize -= 10

            //console.log(this.fsize);
            //console.log(this.counter);

            this.$emit('cc', this.counter)
        },
    },
}
</script>