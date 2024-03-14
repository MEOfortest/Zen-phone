<svelte:head>

<title>Телефоны, ноутбуки, компьютеры</title>
</svelte:head>
<div class="container">
    <h1>Телефоны, ноутбуки, компьютеры</h1>
    <div class="blogposts">
        {#each gadgets as page}
            <div class="post">
                <img src="{page.url}" alt="qwerty" />
                    <h2>{page.title}</h2>
                    <p>{page.body}</p>
                    <p class="readmore">
                        <a class="link" href={`/gadgets/elements/${page.id}`}>
                        Посмотреть все характеристики
                        </a>
                    </p>
            </div>
        {/each}
    </div>
</div>

<script>
    import {gadgets} from "./gadgets";
</script>

<style>
    .container {
        margin: 150 px auto;
        max-width: 1300px;
        padding: 0 20px;
    }

    .blogposts {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-gap: 80px;
    }

    .post {
        border: 3px solid red;
        padding: 10px;
        box-shadow: 0 0 10px #eee;
    }

    .link {
        color: rgb(10,10,139);
    }
</style>