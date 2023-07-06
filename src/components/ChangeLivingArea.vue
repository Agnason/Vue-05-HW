<template>
    <div class="project center">
        <ProjectItem :item="project" v-for="project in projects" :key="project.id">

        </ProjectItem>
    </div>
</template>

<script>
import ProjectItem from './ProjectItem.vue';

export default {
    name: "ChangeLivingArea",

    components: {
        ProjectItem
    },

    data() {
        return {
            projects: [
                {
                    id: 1,
                    imgSrc: require('../assets/livingArea/livingArea_1.jpg'),
                    altSrc: 'livingArea_1',
                    title: 'Modern Living Area',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 2,
                    imgSrc: require('../assets/livingArea/livingArea_2.jpg'),
                    altSrc: 'livingArea_2',
                    title: 'Modern Living Area',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 3,
                    imgSrc: require('../assets/livingArea/livingArea_3.jpg'),
                    altSrc: 'livingArea_3',
                    title: 'Modern Living Area',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 4,
                    imgSrc: require('../assets/livingArea/livingArea_4.jpg'),
                    altSrc: 'livingArea_4',
                    title: 'Modern Living Area',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 5,
                    imgSrc: require('../assets/livingArea/livingArea_5.jpg'),
                    altSrc: 'livingArea_5',
                    title: 'Modern Living Area',
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