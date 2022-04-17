<script>
    import Container from "./Container.svelte";
</script>

<footer>
    <Container>
        <div class="flex">
            <p>Het Mediationhuis &copy;</p>
            <div>
                Icons made by <a href="https://www.freepik.com" title="Freepik">Freepik</a> from
                <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>
            </div>
        </div>
    </Container>
</footer>

<style>
    footer {
        background-color: black;
        padding: 2rem;
        color: white;
    }

    .flex {
        display: flex;
        justify-content: space-between;
    }

    @media screen and (max-width: 768px) {
        .flex {
            flex-direction: column;
            text-align: center;
            gap: 1rem;
        }
    }
</style>
