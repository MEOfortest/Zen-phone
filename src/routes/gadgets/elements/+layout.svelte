<div class="container">
    <a href="/blog">Вернуться назад</a>
    <slot />
</div>

<style>
    .container {
        margin: 70px auto;
        width: 80%;
        padding: 0 20px;
    }

    a {
        border: 2px solid black;
        padding: 5px;
        border-radius: 20%;
    }
</style>