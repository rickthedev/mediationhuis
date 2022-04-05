<script>
    import Container from "./Container.svelte";
</script>

<section class="locatie" id="locatie">
    <div class="background">
        <div class="left" />
        <div class="right" />
    </div>
    <Container>
        <div class="content">
            <h2>De Locatie</h2>
            <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Commodi dolorem architecto odio, natus
                cupiditate eum a voluptates ea quia illo quisquam provident rerum, corporis quasi harum optio eos,
                asperiores laboriosam. Voluptas nisi distinctio ducimus ipsa non voluptatem ea provident vitae?
            </p>
        </div>
    </Container>
</section>

<style>
    .locatie {
        position: relative;

        padding: 2rem 0;
        padding-bottom: 3rem;
    }

    .background {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;

        z-index: -10;

        display: grid;
        grid-template-columns: 1fr 1fr;
    }

    .content {
        width: 50%;
        padding-right: 2rem;

        color: white;
    }

    .left {
        background-color: black;
    }

    .right {
        background-image: url("/src/assets/huis.jpeg");
        background-position: center;
        background-size: cover;
    }
</style>
