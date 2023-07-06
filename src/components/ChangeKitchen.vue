<template>
    <div class="project center">
        <ProjectItem :item="project" v-for="project in projects" :key="project.id">

        </ProjectItem>
    </div>
</template>

<script>
import ProjectItem from './ProjectItem.vue';

export default {
    name: "ChangeKitchen",

    components: {
        ProjectItem
    },
    data() {
        return {
            projects: [
                {
                    id: 1,
                    imgSrc: require('../assets/kitchen/kitchen_1.jpg'),
                    altSrc: 'kitchen_1',
                    title: 'Modern Kitchen',
                    text: 'Decor / Artchitecture',
                    imgIconSrc: require('../assets/icon.svg'),
                    imgIconAlt: 'icon'
                },
                {
                    id: 2,
                    imgSrc: require('../assets/kitchen/kitchen_2.jpeg'),
                    altSrc: 'kitchen_2',
                    title: 'Modern Kitchen',
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