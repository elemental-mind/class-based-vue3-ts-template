# A class based Vue 3 template

I was missing the class based syntax I was used to from Vue 2 where I heavily used `vue-class-component`.

This template sets you up so that you can write your components in such a fashion with Vue 3:

```vue
<template>
    <div class="container">
        <h1>{{ msg }}</h1>
        <button type="button" @click="increment()"> Counter is at: {{ count }}</button>
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
    ...
</style>
```

This repo gives you a fresh start with class components in Vue 3 based on the awesome `vue-facing-decorator`-project. To learn more and get some code samples look here:

[vue-facing decorator](https://facing-dev.github.io/vue-facing-decorator/#/)


## Getting started

Pretty straighforward. Clone this repository, do an `npm install` and start your vite dev-server with `npm run dev`. Your app should be listening on `localhost:3000`.

## A word on debugging

### Initial setup

This repo is set up for `VSCode` and includes a `launch.json` configured to attach to a running edge instance launched with the `--remote-debugging-port=9222` flag.
I am working heavily with the Edge Tools for VSCode as they make the dev experience seamless - hence the setup.

### Debugging issues with HMR

Vite's HMR breaks your breakpoints. Once you hit save and vite replaces a module your breakpoints will stop. To hit the breakpoints properly again you need to unfortunately do a full page reload. Then breakpoints work again until you do the next change.
You can disable HMR in the vite config, hwever this is not an option for me and I found occasional reloading to be a bearable workaround.

