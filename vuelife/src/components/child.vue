<template>
    <div style="background-color: #6495ed">
        <header>我是子组件</header>
        <span>{{year}}</span>
        <button @click="changeTime">时光机</button>
        <br/>
        <button @click="destroy">点我销毁子组件</button>
    </div>
</template>

<script>
    export default {
        name: "child",
        data() {
            return {
                year: '现在是2020年'
            }
        },
        props: ['proptest'],
        methods: {
            changeTime() {
                this.year === '大人，时代变了' ? this.year = '现在是2020年' : this.year = '大人，时代变了'
            },
            methodsAvailable() {

            },
            destroy(){
                this.$destroy()
            }
        },
        computed: {
            time() {
                return Date.now()
            }
        },
        beforeCreate() {
            console.log('------------start-------------')
            console.log('当前是beforeCreate')
            console.log('this', this)
            console.log('el', this.$el)
            console.log('data', this.$data)
            console.log('prop', this.$props)
            console.log('watch', this._watchers)
            console.log('methods', this.methodsAvailable)
            console.log('computed', this.time)
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')
        },
        created() {
            console.log('------------start-------------')
            console.log('当前是created')
            console.log('el', this.$el)
            console.log('data', this.$data)
            console.log('prop', this.$props)
            console.log('watch', this._watchers)
            console.log('methods', this.methodsAvailable)
            console.log('computed', this.time)
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')
        },
        beforeMount() {
            console.log('------------start-------------')
            console.log('当前是beforeMount')
            console.log('el', this.$el)
            console.log('data', this.$data)
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')
        },
        mounted() {
            console.log('------------start-------------')
            console.log('当前是mounted')
            console.log('el', this.$el)
            console.log('data', this.$data)
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')

        },
        beforeUpdate() {
            console.log('------------start-------------')
            console.log('当前是beforeUpdate')
            console.log('el', this.$el.innerHTML)
            console.log('data', JSON.stringify(this.$data))
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')
        },
        updated() {
            console.log('------------start-------------')
            console.log('当前是updated')
            console.log('el', this.$el.innerHTML)
            console.log('data', JSON.stringify(this.$data))
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')
        },
        beforeDestroy() {
            console.log('------------start-------------')
            console.log('当前是beforeDestroy')
            console.log('el', this.$el)
            console.log('data', this.$data)
            console.log('year', this.year)
            console.log('------------end-------------')
            console.log('')
        },
        destroyed() {
            console.log('------------start-------------')
            console.log('当前是destroyed')
            console.log('el', this.$el)
            console.log('data', this.$data)
            console.log('year', this.year)
            console.log('watch', this._watchers)
            console.log('methods', this.methodsAvailable)
            console.log('computed', this.time)
            console.log('------------end-------------')
            console.log('')
        }
    }
</script>

<style scoped>

</style>
