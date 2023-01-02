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
</template>
