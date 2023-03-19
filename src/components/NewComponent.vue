<script setup>
    import { ref } from "vue";

    const name = ref("Alex");
    const showName = false;

    const props = "prop";

    const books = ref([
        {
            title: "KSIAZKA 1"
        },
        {
            title: "KSIAZKA 2"
        },
        {
            title: "KSIAZKA 3"
        }
    ])
</script>

<template>
    <div class="new-compoment">
        <input v-model="name" type="text" placeholder="dodaj imie" />
        <h2>Jestem nowym komponentem {{ name }}</h2>
        <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus quos ratione doloribus accusamus eos dignissimos non exercitationem velit? Ab, est?
        </p>
        
        <h2>Book list:</h2>
        <ul>
            <li v-for="(book, key) in books">
                {{ book.title }}
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
.new-compoment {
    background: blue;
    padding: 20px;
    margin: 10px 0;
}
</style>