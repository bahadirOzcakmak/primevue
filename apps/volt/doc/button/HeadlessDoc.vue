<template>
    <DocSectionText v-bind="$attrs">
        <p>Headless mode is enabled by adding the <i>asChild</i> property and defining your own UI element with the available bindings.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <Button v-slot="slotProps" asChild>
            <button
                v-bind="slotProps.a11yAttrs"
                class="rounded-lg bg-gradient-to-br from-primary-400 to-primary-700 active:from-primary-700 active:to-primary-900 text-white border-none px-6 py-3 font-bold hover:ring-2 cursor-pointer ring-offset-2 ring-offset-surface-0 dark:ring-offset-surface-900 ring-primary transition-all"
            >
                SIGN UP
            </button>
        </Button>
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Button from '@/volt/Button.vue';
import { ref } from 'vue';

const code = ref(`
<template>
    <div class="card flex justify-center">
        <Button v-slot="slotProps" asChild>
            <button
                v-bind="slotProps.a11yAttrs"
                class="rounded-lg bg-gradient-to-br from-primary-400 to-primary-700 active:from-primary-700 active:to-primary-900 text-white border-none px-6 py-3 font-bold hover:ring-2 cursor-pointer ring-offset-2 ring-offset-surface-0 dark:ring-offset-surface-900 ring-primary transition-all"
            >
                SIGN UP
            </button>
        </Button>
    </div>
</template>

<script setup lang="ts">
import Button from '@/volt/Button.vue';
<\/script>
`);
</script>
