<script>
    import Container from "./Container.svelte";
    import IntersectionObserver from "./IntersectionObserver.svelte";
</script>

<section id="vertrouwenspersoon" class="vertrouwenspersoon">
    <Container>
        <h2>Vertrouwenspersoon</h2>

        <div class="narrow">
            <IntersectionObserver>
                <div class="persoon">
                    <div class="photoContainer">
                        <img
                            src="https://images.unsplash.com/photo-1552058544-f2b08422138a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1998&q=80"
                            alt=""
                        />
                    </div>
                    <q>
                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolor iste ut consequatur aliquid
                        veniam repellat, possimus vero accusantium numquam minima consectetur, ipsa harum cum
                        reprehenderit sed, hic odit. Repudiandae, similique!
                    </q>
                </div>
            </IntersectionObserver>

            <div class="info">
                <h3>Ongewenst gedrag</h3>
                <p>
                    Waar mensen werken kunnen ongewenste omgangsvormen ontstaan. Meer dan 1,2 miljoen mensen hebben hier
                    last van. Het gaat dan bijvoorbeeld om: (sexuele) intimidatie, agressie en geweld, pesten,
                    discriminatie of anderen vormen.
                </p>

                <h3>Gevolgen</h3>
                <p>
                    Gevolgen werknemers zijn stress (PTSS), psychische schade, uitval en demotivatie. Gevolgen
                    werkgevers zijn het risico op reputatieschade en mogelijk grote financiele gevolgen
                </p>

                <h3>Vertrouwenspersoon</h3>
                <p>
                    De vertrouwenspersoon kan een cruciale rol spelen bij uw rol als goed werkgever. Zij biedt opvang en
                    begeleiding, Helpt met voorlichten, informeren en inspireren van de medewerkers en de organisatie.
                    Levert gevraagd en ongevraagd advies aan bestuur, directie en/of management. Biedt hulp bij
                    evaluatie en opzetten van beleid. Het huis van Vertrouwenspersonen is er om u te ondersteunen en
                    helpt u en uw medewerkers.
                </p>
            </div>
        </div>
    </Container>
</section>

<style>
    .vertrouwenspersoon {
        background-image: url("/src/assets/safe.png");
        background-position: center;
        background-size: cover;

        padding: 2rem 0;

        color: white;
    }

    .narrow {
        width: 720px;
        margin: 0 auto;
    }

    @media screen and (max-width: 768px) {
        .narrow {
            width: 100%;
        }
    }

    .persoon {
        margin-bottom: 2rem;

        padding: 0rem 2rem 2rem 2rem;
        margin-top: 8.5rem;

        display: flex;
        flex-direction: column;
        align-items: center;

        border: 3px solid white;
    }

    q {
        text-align: justify;
        hyphens: auto;
        font-style: italic;
        font-size: 1.4rem;
    }

    .photoContainer {
        margin-top: -7.5rem;
        width: 15rem;
        height: 15rem;
        border-radius: 1000px;
        overflow: hidden;
        margin-bottom: 2rem;
    }

    @media screen and (max-width: 768px) {
        .photoContainer {
            margin-top: -5rem;
            width: 10rem;
            height: 10rem;
        }
    }

    .photoContainer img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
    }

    .info h3 {
        margin-top: 1rem;
    }

    .info p {
        text-align: justify;
        hyphens: auto;
    }
</style>
