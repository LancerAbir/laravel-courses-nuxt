<template>
    <NuxtPage />
    <header>
        <nav>
            <ul>
                <li><NuxtLink to="/about">About</NuxtLink></li>
                <li><NuxtLink to="/courses">Courses</NuxtLink></li>
            </ul>
        </nav>
    </header>

    <Button />
    <div>
        <h1>Welcome to the homepage</h1>

        <AppAlert> This is an auto-imported component </AppAlert> <br />
    </div>

    <h4>Data Fatching</h4>
    <div v-if="pending">Loading ..........</div>
    <div v-else>
        <ul>
            <li v-for="user in users" :key="user.id">
                {{ user.id }} Title: {{ user.title }}
            </li>
        </ul>
    </div>
</template>

<script setup>
// const { data: count } = await useFetch("/api/count");
const { pending, data: users } = await useFetch(
    "https://jsonplaceholder.typicode.com/todos/"
);

console.log(users.data);
</script>
