<script>
    import Container from "./Container.svelte";
    import logo from '/src/assets/logo/Icon White.svg'
</script>

<nav>
        <ul>
            <li>
                <a href="#header"><img class="logo" src={logo} alt="" /></a>
            </li>
            <li><a href="#mediation">mediation</a></li>
            <li><a href="#vertrouwenspersoon">vertrouwenspersoon</a></li>
            <li><a href="#contact">contact</a></li>
        </ul>
</nav>

<style>
    nav {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
    }

    @media screen and (max-width: 567px) {
        nav {
            display: none;
        }
    }

    ul {
        display: flex;
        align-items: center;
        padding: 3rem;
        color: white;
    }

    li:not(:first-child) {
        margin-left: 3rem;
    }

    @media screen and (max-width: 768px) {
        li:not(:first-child) {
            margin-left: 2rem;
        }
    }

    li:first-child {
        margin-right: auto;
    }

    .logo {
        width: 2.5rem;
        /* height: 2rem; */
    }
</style>
