<script lang="ts">
    let name = '';
    let email = '';
    let message = '';

    async function sendMessage(){}
</script>

<div class="container">
    <div class="touch-container">
        <div>
            <h1>Get in Touch</h1>
        </div>
        <div>
            <p>
                I’d love to hear about what you’re working on and how I could help. I’m currently looking for a new role and am open to a wide range of opportunities. My preference would be to find a position in a company in London. But I’m also happy to hear about opportunities that don’t fit that description. I’m a hard-working and positive person who will always approach each task with a sense of purpose and attention to detail. Please do feel free to check out my online profiles below and get in touch using the form.
            </p>
            <ul class="social-media">
                <li>
                    <a href="/github.com">
                        <img src="/images/icons/github.svg" class="filter" alt="github">
                    </a>
                </li>
                <li>
                    <a href="/twitter.com">
                        <img src="/images/icons/twitter.svg" class="filter" alt="twitter">
                    </a>
                </li>
                <li>
                    <a href="/linkedin.com">
                        <img src="/images/icons/linkedin.svg" class="filter" alt="linkedin">
                    </a>
                </li>
            </ul>
        </div>
    </div>
    
    <div class="contact-container">
        <div>
            <h2>Contact Me</h2>
        </div>
        <div>
            <form on:submit|preventDefault={sendMessage}>
                <label for="name">Name</label>
                <input type="text" id="name" bind:value={name} placeholder="Jane Appleseed" required>
            
                <label for="email">Email Address</label>
                <input type="email" id="email" bind:value='{email}' placeholder="email@example.com" required>
            
                <label for="name">Message</label>
                <textarea id="message" rows="4" bind:value={message} placeholder="How can I help?" required></textarea>
            
                <button type="submit">Send Message</button>
            </form>
        </div>
    </div>
</div>

<style>
    .container{
        margin-top: 2.5rem;
    }

    .touch-container{
        border-top: 1px solid #979797;
        border-bottom: 1px solid #979797;
        padding-bottom: 2rem;
    }

    .touch-container h1 {
        font-size: 2.5rem;
        line-height: 42px;
        letter-spacing: -0.36px;
    }

    .touch-container p {
        line-height: 30px;
        padding-top: 1.5rem;
    }

    ul {
        margin: 0;
        padding: 0;
        list-style-type: none;
        text-align: center;
    }

    li a {
        color: #ffffff;
        text-decoration: none;
    }

    .social-media{
        display: flex;
        align-items: center;
        justify-content: flex-start;
        gap: 1rem;
        margin-top: 2.5rem;
    }

    .contact-container h2{
        font-size: 2.5rem;
    }

    form{
        display: flex;
        flex-direction: column;
        padding-top: 1.5rem;
    }

    label{
        margin-block: 1.5rem .5rem;
    }

    input, textarea {
        background-color: lightgrey;
        border: none;
        margin-top: .5rem;
        padding: 9px 1rem;
        color: #33323D;
    }

    button{
        width: 200px;
        background-color: #203A4C;
        border: none;
        color: #ffffff;
        letter-spacing: 2px;
        padding: 1rem 1.5rem;
        margin-top: 1.5rem;
        font-size: 12px;
    }

    @media only screen and (min-width: 768px){
        .container{
            margin-top: 5.875rem;
            padding-inline: 2.5rem;
        }
    }

    @media only screen and (min-width: 1100px){
        .touch-container{
            display: flex;
            justify-content: space-between;
        }

        .touch-container > div {
            flex: 1;
        }

        .touch-container p {
            padding-top: 0rem;
        }

        .contact-container{
            display: flex;
            justify-content: space-between;
        }

        .contact-container > div {
            flex: 1;
        }

        form{
            padding-top: 0rem;
        }
    }
</style>