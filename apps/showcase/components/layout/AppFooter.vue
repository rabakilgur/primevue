<template>
    <div class="layout-footer">
        <div>
            <span>PrimeVue {{ version }} on Vue 3 by </span>
            <a href="https://www.primetek.com.tr" target="_blank" rel="noopener noreferrer">PrimeTek</a>
        </div>
        <div class="mt-2 text-sm text-surface-500">
            <strong>Disclaimer:</strong> This is not the official PrimeVue page. For the official documentation, visit
            <a href="https://primevue.org" target="_blank" rel="noopener noreferrer">primevue.org</a>.
        </div>
    </div>
</template>

<script>
import pkg from '@/package.json';

export default {
    data() {
        return {
            version: pkg.version
        };
    }
};
</script>
