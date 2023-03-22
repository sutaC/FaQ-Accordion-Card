<script>
    import Faq from "./faq.svelte"


</script>
<!-- ---  -->

<div class="card">
    <div class="images">
        <img src="/illustration-box-desktop.svg" alt="illustration-box">
        <img src="/illustration-woman-online-desktop.svg" alt="illustration-woman-online">
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
    }

    :global(body) {
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }


    .card {
        display: flex;

        width: 40rem;
        height: 30rem;
    }

    
    img {
        width: 100%;
    }

    .questions { 
        width: 50%;
    }


    footer {
        position: fixed;
        bottom: 0;
        width: 100%;
        text-align: center;
        font-size: 10px;
    }
    

</style>