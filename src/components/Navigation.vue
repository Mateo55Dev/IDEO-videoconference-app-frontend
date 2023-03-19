<script setup>
    import {RouterLink} from 'vue-router';
    import IconVideo from './icons/IconVideo.vue';
    import IconChat from './icons/IconChat.vue';
    import IconFriends from './icons/IconFriends.vue';
    import IconSettings from './icons/IconSettings.vue';
</script>

<template>
    <nav>
        <RouterLink class="nav-item" to="/">
            <IconVideo class="nav-icon"></IconVideo>
        </RouterLink>
        <RouterLink class="nav-item" to="/chats">
            <IconChat class="nav-item"></IconChat>
        </RouterLink>
        <RouterLink class="nav-item" to="/friends">
            <IconFriends class="nav-item"></IconFriends>
        </RouterLink>
        <RouterLink class="nav-item" to="/settings">
            <IconSettings class="nav-item"></IconSettings>
        </RouterLink>
    </nav>
</template>

<style lang="scss" scoped>
    nav{
        background-color: #f1f6fa;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>