<script setup>

</script>
<template>
    <header>
    <RouterLink to="/">
        <img class="logo" src="./../assets/logo.png" alt="logo">
    </RouterLink>
    <input class="search" placeholder="search">
    </header>
</template>

<style lang="scss" scoped>
    header{
        display: flex;
        align-items: center;
        gap: 20px;
    .logo{
        width: 80px;
        height: 80px;
        fill: var(--color-primary);
        transition: all 0.2s;
        &:hover{
            transform: scale(1.1);
            filter: brightness(1.1);
        }
    }
    .search{
        background: var(--color-background-gray-dark);
        border: none;
        border-radius: 10px;
        padding: 15px 12px;
        flex-grow: 1;
        @media(max-width: 1299px){
            display: none;
        }
    }
}
</style>