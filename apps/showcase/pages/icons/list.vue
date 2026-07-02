<template>
    <div>
        <Head>
            <Title>Vue Icon Library - PrimeVue</Title>
            <Meta name="description" content="PrimeIcons is the default icon library of PrimeVue with over 250 open source icons developed by PrimeTek. PrimeIcons library is optional as PrimeVue components can use any icon with templating." />
        </Head>

        <div class="doc">
            <div class="doc-main">
                <h1 class="-mb-2">Icon List</h1>
                <DocSections :docs="docs" />
            </div>
        </div>
    </div>
</template>

<script>
import DocCopyMarkdown from '@/components/doc/DocCopyMarkdown.vue';
import ListDoc from '@/doc/icons/ListDoc.vue';

export default {
    components: { DocCopyMarkdown },
    data() {
        return {
            docs: [
                {
                    id: 'list',
                    label: 'List',
                    component: ListDoc
                }
            ]
        };
    }
};
</script>

<style scoped>
.doc-main ::v-deep(.doc-section-label),
.doc-main ::v-deep(.doc-section-description) {
    display: none;
}
</style>
