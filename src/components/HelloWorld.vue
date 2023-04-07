<template>
    <div class="container">
        <h1>{{ msg }}</h1>

        <p>
            Recommended IDE setup:
            <a href="https://code.visualstudio.com/" target="_blank">VSCode</a>
            +
            <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
        </p>

        <p>See <code>README.md</code> for more information.</p>

        <p>
            <a href="https://vitejs.dev/guide/features.html" target="_blank">
                Vite Docs
            </a>
            |
            <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Docs</a>
        </p>

        <button type="button" @click="increment()"> Counter is at: {{ count }}</button>
        <p>
            Change
            <code>components/HelloWorld.vue</code> to test hot module replacement.
        </p>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-facing-decorator';

@Component({ components: {  } })
export default class HelloWorld extends Vue 
{
    @Prop({default: "Default message!"}) 
    msg!: string;
    
    count = 0;
    
    increment()
    {
        this.count++;
    }
}
</script>

<style scoped>
a {
    color: #42b983;
}

label {
    margin: 0 0.5em;
    font-weight: bold;
}

code {
    background-color: #eee;
    padding: 2px 4px;
    border-radius: 4px;
    color: #304455;
}

.container {
    width: 600px;
    margin: auto;
}
</style>