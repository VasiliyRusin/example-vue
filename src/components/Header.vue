<template>
    <header>
        <h1>{{ textSynced }}</h1>
        <button @click="textSynced = ''">Очистить</button>
    </header>
</template>

<script>
    
    export default {
        name: "header",
        props: {
            text: {
                type: String
            }
        },
        
        computed: {
            textSynced: {
                get () {
                    return this.text;
                },
                
                set (value) {
                    this.$emit("update:text", value);
                }
            }
        }
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
    h3 {
        margin: 40px 0 0;
    }
    
    ul {
        padding: 0;
        list-style-type: none;
    }
    
    li {
        margin: 0 10px;
        display: inline-block;
    }
    
    a {
        color: #42B983;
    }
</style>
