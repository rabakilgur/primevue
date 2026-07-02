<template>
    <div :class="containerClass">
        <AppTopBar :showMenuButton="false" />
        <HeroSection />
        <FeaturesSection />
        <UsersSection />
        <ThemeSection />
        <FooterSection />
        <Toast />
    </div>
</template>

<script>
import FeaturesSection from '@/components/landing/FeaturesSection.vue';
import FooterSection from '@/components/landing/FooterSection.vue';
import HeroSection from '@/components/landing/HeroSection.vue';
import ThemeSection from '@/components/landing/ThemeSection.vue';
import UsersSection from '@/components/landing/UsersSection.vue';

export default {
    setup() {
        definePageMeta({
            layout: 'custom'
        });
    },
    props: {
        theme: {
            type: String,
            default: null
        }
    },
    created() {
        this.$appState.designer.active = false;
    },
    computed: {
        containerClass() {
            return ['landing'];
        }
    },
    components: {
        HeroSection,
        ThemeSection,
        UsersSection,
        FeaturesSection,
        FooterSection
    }
};
</script>
