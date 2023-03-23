<script>

    export let hidden = true;

    function hideShow() {
        hidden = hidden ? false : true;
    }

</script>
<!-- ---  -->

<div class="card" class:hidden >
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <div class="header" on:click={hideShow}>
        <p><slot name="question"/></p>
        <img src="/icon-arrow-down.svg" alt="icon-arrow-down" >
    </div>
    <p><slot name="answer"/></p>
</div>

<!-- ---  -->
<style>
    
    .header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 0.5rem;

        cursor: pointer;
        user-select: none;
    }
    
    img {
        width: 1rem;
        height: 0.8rem;
    }

    p {
        font-size: 12px;
    }

    .header > p {
        font-size: 0.9rem;
    }



    .hidden:hover {
        color: hsl(14, 88%, 65%);
    }

    .hidden img {
        transform: rotate(180deg);
    }

    .hidden > p {
        display: none;
    }

    .card:not(.hidden) > .header > p {
        font-weight: 700;
    }



</style>