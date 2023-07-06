<template>
    <div class="project center">
        <ProjectItem :item="project" v-for="project in projects" :key="project.id">

        </ProjectItem>
    </div>
</template>

<script>
import ProjectItem from './ProjectItem.vue';

export default {
    name: "ChangeBedroom",

    components: {
        ProjectItem
    },

    data() {
        return {
            projects: [
                {
                    id: 1,
                    imgSrc: require('../assets/bathroom/bathroom_1.jpg'),
                    altSrc: 'bathroom_1',
                    title: 'Modern Bathroom',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 2,
                    imgSrc: require('../assets/bathroom/bathroom_2.jpg'),
                    altSrc: 'bathroom_2',
                    title: 'Modern Bathroom',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 3,
                    imgSrc: require('../assets/bathroom/bathroom_3.jpg'),
                    altSrc: 'bathroom_3',
                    title: 'Modern Bathroom',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
            ]
        };
    },
    mounted() {
    },
    methods: {},

};
</script>

<style lang="scss" scoped>
.project {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    gap: 104px;
    margin-bottom: 96px;
}
</style>