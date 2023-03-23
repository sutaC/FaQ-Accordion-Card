<script>
    import Faq from "./faq.svelte"
</script>
<!-- ---  -->

<div class="card">
    <div class="images">
        <div class="desktop">
            <div class="img-girl-container">
                <img src="/illustration-woman-online-desktop.svg" alt="illustration-woman-online">
            </div>
            <img src="/illustration-box-desktop.svg" alt="illustration-box" class="img-box">
        </div>
        <div class="mobile">
            <div class="img-girl-container">
                <img src="/illustration-woman-online-mobile.svg" alt="illustration-woman-online">
            </div>
        </div>
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

        height: 100vh;

        background: linear-gradient(hsl(273, 75%, 66%), hsl(240, 73%, 65%));
    }


    .card {
        display: flex;
        gap: 2rem;

        padding: 2rem;

        width: 55rem;
        width: clamp(40%, 55rem, 100%);
        height: 30rem;
        height: clamp(40%, 30rem, 70rem);

        border-radius: 1rem;

        background-color: white;
        box-shadow: 0 0.65rem 0.65rem hsla(0, 0%, 0%, 0.3);
    }


    .questions { 
        width: minmax(50%, 100%);

        padding-right: 2rem;

        overflow: auto;
    }

    .images {
        width: 50%;
        height: minmax(20%, 100%);
    }
    


    /* Images positioning */

    img {
        width: 100%;
        user-select: none;
    }


    .desktop > .img-box {
        width: 10rem;

        transform: translate(-6.9rem, -13rem);
    }

    .desktop > .img-girl-container {
        transform: translate(-4.5rem, 2.5rem) scale(1.25);

        padding-bottom: 5rem;

        background-image: url('/bg-pattern-desktop.svg');
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }

    .desktop > .img-girl-container img {
        object-fit: cover;
        object-position: -4.5rem 0;
        transform: translate(4.5rem, 1.5rem);
    }

    
    .mobile {
        display: none;
    }


    footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        text-align: center;
        font-size: 10px;
    }
    


    /* Mobile */

    @media (max-width: 950px) { 

        .card {
            flex-direction: column;
        }

        .images {
            height: 20%;

        }

        .desktop {
            display: none;
        }

        .mobile {
            display: block;
        }

        .mobile .img-girl-container {
            transform: translate(50%, 0) scale(1.8);

            width: 10rem;

            padding-bottom: 4.5rem;

            background-image: url('/bg-pattern-mobile.svg');
            background-repeat: no-repeat;
            background-position: center;
            background-size: contain;
        }

    }

</style>