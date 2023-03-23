<script>
    import Faq from "./faq.svelte"
</script>
<!-- ---  -->

<div class="card">
    <div class="images">
        <div class="img-girl-container">
            <img src="/illustration-woman-online-desktop.svg" alt="illustration-woman-online">
        </div>
        <img src="/illustration-box-desktop.svg" alt="illustration-box" class="img-box">
    </div>
    <div class="questions">

        <h1>FAQ</h1>

        <Faq>
            <svelte:fragment slot="question">How many team members can I invite?</svelte:fragment>
            <svelte:fragment slot="answer">You can invite up to 2 additional users on the Free plan. There is no limit on team members for the Premium plan.</svelte:fragment>
        </Faq>
        
        <Faq hidden={false}>
            <svelte:fragment slot="question">What is the maximum file upload size?</svelte:fragment>
            <svelte:fragment slot="answer">No more than 2GB. All files in your account must fit your allotted storage space.</svelte:fragment>
        </Faq>
        
        <Faq>
            <svelte:fragment slot="question">How do I reset my password?</svelte:fragment>
            <svelte:fragment slot="answer">Click “Forgot password” from the login page or “Change password” from your profile page. A reset link will be emailed to you.</svelte:fragment>
        </Faq>
        
        <Faq>
            <svelte:fragment slot="question">Can I cancel my subscription?</svelte:fragment>
            <svelte:fragment slot="answer">Yes! Send us a message and we’ll process your request no questions asked.</svelte:fragment>
        </Faq>
        
        <Faq>
            <svelte:fragment slot="question">Do you provide additional support?</svelte:fragment>
            <svelte:fragment slot="answer">Chat and email support is available 24/7. Phone lines are open during normal business hours.</svelte:fragment>
        </Faq>
    </div>
</div>



<footer>
  Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
  Coded by <a href="#sutaC">Your Name Here</a>.
</footer>

<!-- ---  -->
<style>
    @import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap');

    * {
        font-family: 'Kumbh Sans', sans-serif;
        color: hsl(238, 29%, 16%);
    }

    :global(body) {
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        height: 100vh;

        background: linear-gradient(hsl(273, 75%, 66%), hsl(240, 73%, 65%));
    }


    .card {
        display: flex;
        gap: 2rem;

        padding: 2rem;

        width: 55rem;
        height: 30rem;

        border-radius: 1rem;

        background-color: white;
        box-shadow: 0 0.65rem 0.65rem hsla(0, 0%, 0%, 0.3);
    }


    .questions { 
        width: 50%;

        padding-right: 2rem;

        overflow: auto;
    }

    .images {
        width: 50%;
    }
    


    /* Images positioning */

    img {
        width: 100%;
        user-select: none;
    }

    .img-box {
        width: 10rem;

        z-index: 10;

        transform: translate(-6.9rem, -13rem);
    }

    .img-girl-container {
        transform: translate(-4.5rem, 2.5rem) scale(1.25);

        padding-bottom: 5rem;

        background-image: url('/bg-pattern-desktop.svg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }

    .img-girl-container img {
        object-fit: cover;
        object-position: -4.5rem 0;
        transform: translate(4.5rem, 1.5rem);
    }



    footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        text-align: center;
        font-size: 10px;
    }
    

</style>