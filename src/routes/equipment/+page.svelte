<svelte:head>

<title>Холодильники, пылесосы, микроволновки и чайники</title>
</svelte:head>
<div class="container">
    <h1>Холодильники, пылесосы, микроволновки и чайники</h1>
    <div class="blogposts">
        {#each blocks as page}
            <div class="post">
                <h2>{page.title}</h2>
                <p>{page.body}</p>
                <p class="readmore">
                    <a class="link" href={`/equipment/facilities/${page.id}`}>
                    Посмотреть все характеристики
                    </a>
                </p>
            </div>
        {/each}
    </div>
</div>

<script>
    import {facilities} from "./facilities";
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
        border: 3px solid purple;
        padding: 10px;
        box-shadow: 0 0 10px #eee;
    }

    .link {
        color: rgb(10,10,139);
    }
</style>