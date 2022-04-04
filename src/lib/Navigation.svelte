<script>
    import Container from "./Container.svelte";
    import logo from '/src/assets/logo/Icon White.svg'
</script>

<nav>
    <Container>
        <ul>
            <li>
                <a href=""><img class="logo" src={logo} alt="" /></a>
            </li>
            <li><a href="">mediation</a></li>
            <li><a href="">vertrouwenspersoon</a></li>
            <li><a href="">contact</a></li>
        </ul>
    </Container>
</nav>

<style>
    nav {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
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

    li:first-child {
        margin-right: auto;
    }

    .logo {
        width: 2.5rem;
        /* height: 2rem; */
    }
</style>
