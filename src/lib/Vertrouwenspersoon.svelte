<script>
    import Container from "./Container.svelte";
    import IntersectionObserver from "./IntersectionObserver.svelte";
</script>

<section id="vertrouwenspersoon" class="vertrouwenspersoon">
    <Container>
        <h2>Vertrouwenspersoon</h2>

        <div class="half">
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
                <h3>Lorem, ipsum dolor.</h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita mollitia quae inventore laboriosam
                    quaerat aliquid nostrum, recusandae possimus enim, debitis quos beatae veniam. Autem, obcaecati
                    veniam? Possimus consequatur ab beatae!
                </p>

                <h3>Lorem ipsum dolor sit.</h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda labore voluptatem officia
                    repellendus sit consectetur voluptatibus aspernatur explicabo iure quas, ad earum minus deleniti
                    distinctio possimus illum harum quisquam optio, magnam ab excepturi. Assumenda similique, ea porro
                    culpa doloremque suscipit molestiae ipsa ex iusto sit quibusdam expedita dolor possimus natus?
                </p>
            </div>
        </div>
    </Container>
</section>

<style>
    .vertrouwenspersoon {
        background-image: linear-gradient(rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.8)),
            url("/src/assets/photo-1582139329536-e7284fece509.avif");
        background-position: center;
        background-size: cover;

        padding: 2rem 0;
        padding-bottom: 3rem;

        color: white;
    }

    .half {
        width: 50%;
        margin: 0 auto;
    }

    .persoon {
        margin-bottom: 2rem;

        padding: 0rem 2rem 2rem 2rem;
        margin-top: 7.5rem;

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
