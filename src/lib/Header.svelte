<script>
    import Navigation from "./Navigation.svelte";
    import logoUrl from '/src/assets/logo/Icon White.svg'
</script>

<header>
    <Navigation />
    <div class="content">
        <img class="logo" src={logoUrl} alt="" />
        <h1>Het Mediationhuis</h1>
    </div>
    <div class="scroll">
        <img class="mouse" src="/src/assets/iconmonstr-mouse-6.svg" alt="">
        <p>scroll omlaag</p>
    </div>
</header>

<style>
    header {
        position: relative;

        height: 100vh;
        width: 100vw;

        background-image: url("/src/assets/backimage.png");
        background-position: center;
        background-size: cover;

        animation-name: zoom;
        animation-duration: 10s;
        animation-timing-function: cubic-bezier(0, 0.5, 0.5, 1);

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .content {
        display: flex;
        flex-direction: column;
        align-items: center;

        animation-name: fade;
        animation-duration: 5s;
    }

    .logo {
        width: 10rem;
        margin-bottom: 2rem;
    }

    h1 {
        color: white;
        font-size: 5rem;

        user-select: none;
    }

    .scroll {
        display: flex;
        flex-direction: column;
        align-items: center;

        position: absolute;
        bottom: 0;

        margin-bottom: 2rem;
    }

    .scroll p {
        color: white;
    }

    .mouse {
        margin-bottom: 1rem;
        width: 2rem;

        animation-name: bop;
        animation-duration: 2s;
        animation-iteration-count: infinite;
        animation-timing-function: cubic-bezier(0.445, 0.05, 0.55, 0.95);
    }

    @keyframes bop {
        0% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(5px);
        }
        100% {
            transform: translateY(0);
        }
    }

    @keyframes fade {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }

    @keyframes zoom {
        from {
            background-size: 125vw;
        }
        to {
            background-size: 100vw;
        }
    }
</style>
