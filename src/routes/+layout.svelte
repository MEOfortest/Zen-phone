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
         title: "Гаджеты",
         href: "/gadgets",
        },
        {
         title: "Техника",
         href: "/equipment",
        },
        {
         title: "Мебель",
         href: "/furniture",
        },
        {
         title: "О нас",
         href: "/about",
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

    .link {
        font-family: cursive;
    }
</style>