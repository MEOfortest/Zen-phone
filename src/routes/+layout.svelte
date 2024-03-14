<nav>
    <div class="nav-container">
        <div class="nav-links">
            {#each nav as link} 
            <a href={link.href} class="link">{link.title}</a>
            {/each}
        </div>
    </div>
</nav>

<div class="container">
    <slot></slot>
</div>

<script>
    const nav = [
        {
         title: "Главная",
         href: "/",
        },
        {
         title: "О нас",
         href: "/about",
        },
        {
         title: "Блог",
         href: "/blog",
        },
        {
         title: "Новости",
         href: "/news",
        },
        {
         title: "Контакты",
         href: "/contacts",
        },
    ];
</script>

<style>
    .container {
        max-width: 90%;
        margin: 50px auto;
    }

    .nav-container {
        background-color: orange;
        border: 4px solid blue;
        height: 60px;
    }

    a {
        font-size: 35px;
        font-family: cursive;
        align-items: center;
        text-align: center;
    }
</style>