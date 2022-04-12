<script>
    import Container from "./Container.svelte";
    import IntersectionObserver from "./IntersectionObserver.svelte";

    import trusted from "/src/assets/icons/trusted.png";
    import negotiation from "/src/assets/icons/negociation.png";
    import friends from "/src/assets/icons/friends.png";
    import argue from "/src/assets/icons/argue.png";
</script>

<section id="mediation" class="mediation">
    <Container>
        <h2>Mediation</h2>

        <div class="grid">
            <IntersectionObserver transitionDelay={0}>
                <div class="card element">
                    <img src={negotiation} alt="" />
                    <h3>Wat is het?</h3>
                    <p>
                        Mediation is een methode om conflicten en spanningen tussen mensen op te lossen of acceptabel te
                        krijgen. Samenwerking is belangrijk om naar een oplossing te zoeken die werkt voor beiden
                        deelnemers. De deelnemers bepalen het traject.
                    </p>
                </div>
            </IntersectionObserver>

            <IntersectionObserver transitionDelay={0.1}>
                <div class="card element">
                    <img src={trusted} alt="" />
                    <h3>Onpartijdig</h3>
                    <p>
                        De mediator begeleidt en ondersteunt het gesprek, zij is neutraal en onpartijdig. Om vrijuit te
                        kunnen praten en alles te kunnen bespreken is vertrouwelijkheid van groot belang.
                    </p>
                </div>
            </IntersectionObserver>

            <IntersectionObserver transitionDelay={0.2}>
                <div class="card element">
                    <img src={friends} alt="" />
                    <h3>Samen</h3>
                    <p>
                        Het Mediationhuis is er om u te ondersteunen en begeleiden bij conflicten of spanningen. Wilt u
                        niet de juridische weg bewandelen die vaak tijdrovend, kostbaar en balastend is voor de
                        betrokkenen, maar kiest u ervoor om er samen uit te komen dan kunt u bij ons terecht.
                    </p>
                </div>
            </IntersectionObserver>
        </div>
    </Container>
</section>

<style>
    .mediation {
        padding: 2rem 0;
        background-image: url("/src/assets/annie-spratt-hX_hf2lPpUU-unsplash(1).jpg");
        background-size: cover;
        background-position: center;
    }

    h2 {
        margin-bottom: 2rem;
    }

    .grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 2rem;
    }

    @media screen and (max-width: 1200px) {
        .grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media screen and (max-width: 768px) {
        .grid {
            grid-template-columns: repeat(1, 1fr);
        }
    }

    .card {
        height: 100%;
        background-color: white;
        box-shadow: 3px 3px 36px rgba(0, 0, 0, 0.1);

        padding: 2rem;

        text-align: justify;
        hyphens: auto;
    }

    .element {
        text-align-last: center;
    }

    .element img {
        width: 5rem;
        margin-bottom: 1rem;
        margin-top: 1rem;
    }

    .main {
        margin-top: 2rem;
    }

    .main p:not(:last-child) {
        margin-bottom: 1rem;
    }
</style>
