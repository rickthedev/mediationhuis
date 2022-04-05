<script>
    import Container from "./Container.svelte";
</script>

<section id="contact" class="contact">
    <Container>
        <h2>Contact</h2>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsam quaerat libero aut mollitia eum pariatur
            facilis, amet ratione quisquam et perferendis dolore. Molestiae quasi ullam modi unde adipisci, dolore
            praesentium!
        </p>
        <a href="" class="button">mail@example.com</a>
    </Container>
</section>

<style>
    .contact {
        padding: 3rem 0;
    }

    .button {
        display: inline-block;
        padding: 1rem 3rem;
        border: 1px solid black;
        margin-top: 1rem;
        transition: 0.1s cubic-bezier(0.445, 0.05, 0.55, 0.95);
    }

    .button:hover {
        background-color: black;
        color: white;
    }
</style>
