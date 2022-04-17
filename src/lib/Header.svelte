<script>
    import { onMount } from "svelte";
    import { fade } from "svelte/transition";

    import Navigation from "./Navigation.svelte";

    import logo from "/src/assets/logo/Icon White.svg";
    import mouseIcon from "/src/assets/iconmonstr-mouse-6.svg";

    let scrollIndicator;

    let mediationhuisVisible;

    onMount(() => {
        window.onscroll = () => {
            if (window.scrollY > 0) {
                scrollIndicator.style.opacity = "0";
            } else {
                scrollIndicator.style.opacity = "1";
            }
        };
    });

    mediationhuisVisible = true;

    setInterval(() => {
        mediationhuisVisible = !mediationhuisVisible
    }, 5000);

</script>

<header>
    <img
        src="https://images.unsplash.com/photo-1453888768187-1e6746aba265?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2074&q=80"
        alt=""
        class="background"
    />
    <Navigation />
    <div class="content">
        <img class="logo" src={logo} alt="" />
        {#if mediationhuisVisible}
            <h1 in:fade="{{duration: 1000}}">Het Mediationhuis</h1>
        {:else}
            <h1 in:fade="{{duration: 1000}}">Het Huis van Vertrouwenspersonen</h1>
        {/if}
    </div>
    <div class="scroll" bind:this={scrollIndicator}>
        <img class="mouse" src={mouseIcon} alt="" />
        <p>scroll omlaag</p>
    </div>
</header>

<style>
    header {
        position: relative;

        height: 100vh;
        width: 100vw;

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        overflow: hidden;
    }

    .background {
        position: absolute;
        width: 100%;
        height: 100%;

        object-fit: cover;

        z-index: -10;

        animation-name: zoom;
        animation-duration: 10s;

        filter: brightness(0.25);
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

    @media screen and (max-width: 768px) {
        .logo {
            width: 8rem;
        }
    }

    h1 {
        color: white;
        font-size: 4rem;

        user-select: none;

        text-align: center;
    }

    @media screen and (max-width: 1200px) {
        h1 {
            font-size: 3rem;
        }
    }

    @media screen and (max-width: 992px) {
        h1 {
            font-size: 2.5rem;
        }
    }

    @media screen and (max-width: 768px) {
        h1 {
            font-size: 2rem;
        }
    }

    @media screen and (max-width: 576px) {
        h1 {
            font-size: 1.5rem;
        }
    }

    .scroll {
        display: flex;
        flex-direction: column;
        align-items: center;

        position: absolute;
        bottom: 0;

        margin-bottom: 2rem;

        transition: 0.3s;
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
            transform: scale(1.25);
        }
        to {
            transform: scale(1);
        }
    }
</style>
