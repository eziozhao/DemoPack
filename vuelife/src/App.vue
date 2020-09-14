<template>
    <div id="app">
        <header>我是父组件</header>
        <button @click="show=true">点我创建子组件</button>
        <br/>
        <child v-if="show" proptest="属性值"></child>
    </div>
</template>

<script>
    import child from "@/components/child";

    export default {
        name: 'App',
        data() {
            return {
                show: false
            }
        },
        components: {
            child
        },

    }
</script>

<style>
    #app{
        text-align: center;
        background-color: aquamarine;
    }
</style>
