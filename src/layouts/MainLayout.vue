<script setup>
import Navigation from '../components/Navigation.vue';
import Header from '../components/Header.vue';
import Groups from '../components/Groups.vue';
import Friends from '../components/Friends.vue';
import Moments from '../components/Moments.vue';
</script>

<template>
    <div class="main-layout">
        <aside class="aside-left">
            <Header class="pb-5"></Header>
            <Groups class="p-5"></Groups>
            <Friends class="p-5"></Friends>
        </aside>
        <main>
            <div class="container">
                <Navigation></Navigation>
            <slot/>
        </div>
        </main>
        <aside class="aside-right">
            <h1>Aside</h1>
        </aside>
    </div> 
</template>

<style lang="scss" scoped>
 .main-layout{
    display: grid;
    grid-template-columns: 100px 1fr 400px;
    min-height: 100vh;
    @media(min-width: 1300px)
    {
        grid-template-columns: 350px 1fr 400px;
    }
    @media(min-width: 1500px)
    {
        grid-template-columns: 400px 1fr 500px;
    }
}
.aside-left{
    background-color: #f1f6fa;
    padding: 20px 40px;
    min-height: 100vh;
    @media(max-width: 1299px)
    {
        padding: 20px 18px;
    }
}
.aside-right{
    background-color: #f1f6fa;
    padding: 20px 40px;
    min-height: 100vh;
    @media(max-width: 1299px)
    {
        padding: 20px 18px;
    }
}
</style>