<script setup>
import {ref} from "vue"
    const friends = ref([
    {
        name: "Alvin Northouse",
        image: "https://minimaltoolkit.com/images/randomdata/female/107.jpg",
        isActive: "true",
        lastSeen: "2 hour ago"
    },
    {
        name: "Addie Heseltine",
        image: "",
        isActive: "false",
        lastSeen: "2 hour ago",
    },
    {
        name: "Loria Clevinger",
        image: "https://randomuser.me/api/portraits/women/46.jpg",
        isActive: "true",
        lastSeen: "1 hour ago",
    },
    {
        name: "Stanley Tasher",
        image: "https://minimaltoolkit.com/images/randomdata/male/54.jpg",
        isActive: "false",
        lastSeen: "1 hour ago",
    },
    {
        name: "Dennie Treffinger",
        image: "https://randomuser.me/api/portraits/women/43.jpg",
        isActive: "false",
        lastSeen: "1 hour ago",
    },
    {
        name: "Carolee Vanas",
        image: "https://randomuser.me/api/portraits/women/28.jpg",
        isActive: "true",
        lastSeen: "2 hour ago",
    },
    {
        name: "Maryalice Fellion",
        image: "https://minimaltoolkit.com/images/randomdata/female/40.jpg",
        isActive: "true",
        lastSeen: "1 hour ago",
    },
    ]);
</script>
<template>
    <section class="your-friends">
        <span class="section-title"> Your Friends </span>
        <div class="section-content">
            <div v-for="(friend, index) in friends" :key="index" class="friend-item">
                <div class="friend-image">
                    <img :src="friend.image" :alt="friend.name">
                </div>
                <div class="friend-title">
                    {{ friend.name }}
                </div>
                <div v-if="friend.isActive" class="active-dot"></div>
                <div v-else class="last-seen">{{ friend.lastSeen }}</div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    .section-title{
        @media(max-width: 1299px){
            display: none !important;
        }
    }
    .your-friends{

    }
</style>