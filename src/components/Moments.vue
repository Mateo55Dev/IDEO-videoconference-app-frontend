<script setup>
    import {ref} from "vue"
    const showNewRing = ref(false);
    const stories = ref([
    {
        name: "Laree",
        image: "https://minimaltoolkit.com/images/randomdata/female/107.jpg",
        isNew: "true",
    },
    {
        name: "Duane",
        image: "https://minimaltoolkit.com/images/randomdata/male/31.jpg",
        isNew: "false",
    },
    {
        name: "Loria",
        image: "ttps://randomuser.me/api/portraits/women/46.jpg",
        isNew: "true",
    },
    {
        name: "Arianne",
        image: "https://minimaltoolkit.com/images/randomdata/female/9.jpg",
        isNew: "false",
    },
    {
        name: "Dennie",
        image: "ttps://randomuser.me/api/portraits/women/43.jpg",
        isNew: "false",
    },
    {
        name: "Carolee",
        image: "https://randomuser.me/api/portraits/women/28.jpg",
        isNew: "falsee",
    },
    {
        name: "Maryalice",
        image: "https://minimaltoolkit.com/images/randomdata/female/40.jpg",
        isNew: "false",
    },
    ]);

    onMounted(() => {
        setTimeout(() => {
            showNewRing.value = true;
        }, 1000);
    });
</script>

<template>
    <div class="stories">
        <div v-for="{story, index} in stories" :key="index" class="story">
            <div class="story-image" :class={new:story.isNew}>
                <img :src="story.image" :alt="story.name">
                <span class="story-name">{{ story.name }}</span>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .stories{
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        margin-top: -10px;
        .story{
            display: flex;
            align-items: center;
            flex-direction: column;
        }
        .story-image{
            width: 80px;
            height: 80px;
            border-radius: 50%;
            overflow: hidden;
            box-shadow: 3px 4px 7px 8px #0000002e;
            border: 2px solid white;
            transition: border 0.4s ease-in-out;
            &.new{
                border: 4px solid var(--color-secondary)
            }
            img{
                width: 100%;
                height: 100%;
            }
        }
    }

    .story-name{
        font-size: 14px;
        font-weight: 500;
        color: var(--color-text-primary);
        margin-top: 10px;
    }
</style>