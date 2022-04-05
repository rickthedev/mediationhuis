<script>
    import { onMount } from "svelte";

    export let transitionDelay = 0;

    let element;

    let visible = false;

    let observer = new IntersectionObserver(
        (entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    visible = true;
                    element.style.opacity = "1";
                }
            });
        },
        { threshold: 1.0 }
    );

    onMount(() => {
        observer.observe(element);
        element.style.opacity = "0";
        element.style.transition = ".5s";
        element.style.transitionDelay = `${transitionDelay}s`
    });
</script>

<div class="observer">
    <div class="element" bind:this={element}>
        <slot />
    </div>
</div>

<style>
    .element {
        height: 100%;
    }
</style>
