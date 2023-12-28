<script>
    import Modal from '../lib/components/Modal.svelte';

    let showModal = true;
    let mail = 'llll@gmail.com'
</script>
<!-- Sign-up form start -->
<img class="heroimg" src="./images/illustration-sign-up-mobile.svg" alt="">

<article>
    <h1>
        Stay updated!
    </h1>

    <h2>
        Join 60,000+ product managers receiving monthly updates on:
    </h2>

    <ul>
        <li>
            <span>Product discovery and building what matters</span>
        </li>
        <li>
            <span>Measuring to ensure updates are a success</span>
        </li>
        <li>
            <span>And much more!</span>
        </li>
    </ul>

    <form method="POST">
        <label>
            <p>Email address</p>
            <input bind:value="{mail}" name="email" type="email" placeholder="email@company.com" required>
        </label>
        <button on:click={()=> (showModal = true)}>Subscribe to monthly newsletter</button>
    </form>

    <!-- Sign-up form end -->



    <!-- Success message start -->

    <Modal bind:showModal>
        <div slot="header" class="header">
            <img class="imgmodal" src="./images/icon-list.svg" alt="">
            <h1>Thanks for subscribing!</h1>
        </div>

        <ol class="definition-list">
            <li>of or relating to modality in logic</li>
            <li>
                containing provisions as to the mode of procedure or the manner of taking effect —used of a
                contract or legacy
            </li>
            <li>of or relating to a musical mode</li>
            <li>of or relating to structure as opposed to substance</li>
            <li>
                of, relating to, or constituting a grammatical form or category characteristically indicating
                predication
            </li>
            <li>of or relating to a statistical mode</li>
        </ol>

        <a href="https://www.merriam-webster.com/dictionary/modal">merriam-webster.com</a>
    </Modal>

    Thanks for subscribing!

    A confirmation email has been sent to ash@loremcompany.com.
    Please open it and click the button inside to confirm your subscription.

    Dismiss message

    <!-- Success message end -->
</article>


<div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
    Coded by <a href="/">Your Name Here</a>.
</div>


<style>
    .header img {
        width: auto;
        height: 60px;
    }

    .heroimg {
        width: 100%;
        height: 100%;
    }

    ul {
        list-style-image: url('./images/icon-list.svg');

        margin-left: 2rem;
    }

    ul li {
        margin: 1rem 0;
    }

    article {
        padding: 1rem;
        color: var(--darkSlateGrey);
        max-width: 370px;
        margin: 0 auto;
    }

    article h1 {
        font-size: 2.5rem;
        padding: 1rem 0;
    }

    article h2 {
        font-size: 1rem;
        font-weight: 400;
        margin-bottom: 1rem;
    }

    form p {
        font-weight: 700;
    }

    form input {
        padding: 5px;
        border-radius: 5px;

    }

    .imgmodal {
        width: 100%;
        height: 50px;
    }

    @media (min-width: 375px) {
        * {
            border: solid red 1px;
        }
    }
</style>