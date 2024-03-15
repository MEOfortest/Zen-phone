<svelte:head>

<title>Телефоны, ноутбуки, компьютеры</title>
</svelte:head>
<div class="container">
    <h1>Телефоны, ноутбуки, компьютеры</h1>
    <div class="blogposts">
        {#each gadgets as page}
            <div class="post">
                <img src="{page.preview}" width="50%" alt="Preview" />
                    <h2>{page.title}</h2>
                    <p class="price">{page.price}</p>
                    <p class="allcharacteristics">
                        <a class="link" href={`/gadgets/elements/${page.id}`}>
                        Посмотреть все характеристики
                        </a>
                    </p>
            </div>
        {/each}
    </div>
</div>

<a href="/gadgets" title="Вернуться к началу" class="topbutton">^</a>

<script>
    import {gadgets} from "./gadgets";
</script>

<style>
    .container {
        margin: 100 px auto;
        max-width: 90%;
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
        text-align: center;
    }

    .link {
        color: rgb(10,10,139);
    }

    .price {
        font-family: cursive;
    }

    .topbutton {
    text-decoration: none;
    width: 50px;
    height: 50px;
    border: 2px solid black;
    background-color: orange;
    color: red;
    text-align: center;
    position: fixed;
    bottom: 40px;
    right: 40px;
    font-size: 60px;
    border-radius: 100%;
    cursor: pointer;
}
</style>