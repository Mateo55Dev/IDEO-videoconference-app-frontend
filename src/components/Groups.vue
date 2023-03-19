<script setup>
const groups = ref([
    {
        title: "Programming",
        image: 'https://picsum.photos/100',
    },
    {
        title: "Gaming",
        image: 'https://picsum.photos/80',
    },
]);
</script>

<template>
    <section class="your-groups">
        <span class="section-title">Your groups</span>
        <div class="groups-list">

            <div v-for="(group, index) in groups" class="group-item">
                <div class="group-image">
                    <img src="group-image">
                </div>
                <div class="group-title">{{group.title}}</div>
            </div>
    
        </div>
    </section>
</template>-->

<style lang="scss" scoped>
    .section-title{
        @media(max-width: 1299px){
            display: none !important;
        }
    }
    .your-groups{
        @media(max-width: 1299px){
            border-bottom: 1px solid #e7e7e7;;
        }
    }
    .groups-list{
        display: flex;
        gap: 20px;
        flex-direction: column;
    }
</style>