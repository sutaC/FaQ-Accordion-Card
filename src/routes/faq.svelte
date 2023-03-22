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
        <h2><slot name="question"/></h2>
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
    }
    
    h2 {
        font-size: 0.9rem;
    }
    
    img {
        width: 1rem;
        height: 0.8rem;

        cursor: pointer;
    }

    p {
        font-size: 12px;
    }



    .hidden img {
        transform: rotate(180deg);
    }

    .hidden p {
        display: none;
    }

</style>