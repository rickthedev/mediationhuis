<script>
    import { onMount } from "svelte";

    import Container from "./Container.svelte";
    import IntersectionObserver from "./IntersectionObserver.svelte";

    import trusted from "/src/assets/icons/001-trusted.png";
    import negotiation from "/src/assets/icons/002-negociation.png";
    import friends from "/src/assets/icons/003-friends.png";
</script>

<section id="mediation" class="mediation">
    <Container>
        <h2>Mediation</h2>

        <div class="triple">
            <IntersectionObserver transitionDelay={0}>
                <div class="element">
                    <img src={trusted} alt="" />
                    <h3>Gecertificeerd</h3>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Reiciendis consequuntur pariatur
                        nesciunt tempore repellendus deserunt mollitia animi amet, sed accusantium.
                    </p>
                </div>
            </IntersectionObserver>

            <IntersectionObserver transitionDelay={0.1}>
                <div class="element">
                    <img src={negotiation} alt="" />
                    <h3>In Gesprek</h3>
                    <p>
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut laboriosam hic neque, ipsum numquam
                        adipisci maxime dolorem aliquid aut id vitae excepturi, architecto cumque delectus sapiente cum
                        recusandae vero! Beatae!
                    </p>
                </div>
            </IntersectionObserver>

            <IntersectionObserver transitionDelay={0.2}>
                <div class="element">
                    <img src={friends} alt="" />
                    <h3>Vriendelijk</h3>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, molestiae?</p>
                </div>
            </IntersectionObserver>
        </div>
    </Container>
</section>

<style>
    .mediation {
        padding: 2rem 0;
        padding-bottom: 3rem;
        background-image: url("/src/assets/annie-spratt-hX_hf2lPpUU-unsplash(1).jpg");
        background-size: cover;
        background-position: center;
    }

    h2 {
        margin-bottom: 2rem;
    }

    .triple {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 2rem;
    }

    .element {
        height: 100%;

        text-align: justify;
        text-align-last: center;
        hyphens: auto;

        background-color: white;

        box-shadow: 3px 3px 36px rgba(0, 0, 0, 0.1);
        border-radius: 0.2rem;
        padding: 2rem;
    }

    .element img {
        width: 4rem;
        margin-bottom: 1rem;
    }
</style>
