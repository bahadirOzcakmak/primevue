<template>
    <DocSectionText v-bind="$attrs">
        <p>When <i>disabled</i> is present, the element cannot be used.</p>
    </DocSectionText>
    <div class="card flex justify-center">
        <Button label="Submit" disabled />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import Button from '@/volt/Button.vue';
import { ref } from 'vue';

const code = ref(`
<template>
    <div class="card flex justify-center">
        <Button label="Submit" disabled />
    </div>
</template>

<script setup lang="ts">
import Button from '@/volt/Button.vue';
<\/script>
`);
</script>
