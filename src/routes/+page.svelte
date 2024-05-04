<script>
	import Button from "$lib/components/shared/Button.svelte";
    import Interested from "$lib/components/shared/Interested.svelte";
</script>

<div class="container">
    <div class="hero-container">
        <picture>
            <source media="(min-width: 1100px)" srcset='/images/homepage/desktop/image-homepage-hero.jpg'>
            <source media="(min-width: 768px)" srcset='/images/homepage/tablet/image-homepage-hero.jpg'>
            <img src='/images/homepage/mobile/image-homepage-hero.jpg' alt="hero">
        </picture>
        <div class="hero-heading">
            <h1>Hey, I’m Graeme Byrne and I love building beautiful websites</h1>
            <div class="btn-container">
                <img src="/images/icons/down-arrows.svg" alt="down arrows">
                <a href="#about" id="about">
                    ABOUT ME
                </a>
            </div>
        </div>
    </div>
    <div class="about-me-container">
        <picture>
            <source media="(min-width: 1100px)" srcset='/images/homepage/desktop/image-homepage-profile.jpg'>
            <source media="(min-width: 768px)" srcset='/images/homepage/tablet/image-homepage-profile.jpg'>
            <img src='/images/homepage/mobile/image-homepage-profile.jpg' alt="hero">
        </picture>
        <div class="about-me-container-text">
            <h2 id="about">About Me</h2>
            <p>
                I’m a front-end developer looking for a new role in an exciting company. I focus on writing accessible HTML, using modern CSS practices and writing clean JavaScript. When writing JavaScript code, I mostly use SvelteKit or React, but I can adapt to whatever tools are required. I’m based in Barcelona, Spain, but I’m happy working remotely and have experience in remote teams. When I’m not coding, you’ll find me outdoors. I love staying active whether that’s playing football, going for a run or cycling around the city. I’d love you to check out my work.
            </p>
            <Button
                link={'/portfolio'}
                text={'Go to Portfolio'}
            />
        </div>
    </div>
</div>
<Interested />

<style>
    .container{
        margin-inline: 2rem;
    }

    .hero-container{
        margin-top: 2.5rem;
    }

    h1, h2{
        font-size: 2.5rem;
        font-weight: bold;
        line-height: 2.625rem;
        letter-spacing: -0.36px;
        margin-top: 1.5rem;
        color: #33323D;
    }

    .btn-container{
        display: flex;
        justify-content: flex-start;
        align-items: center;
        gap: 4rem;
        margin-top: 2rem;
        background-color: #203A4C;
        border: none;
        width: 200px;
        padding: 1rem;
    }

    .btn-container a {
        color: #ffffff;
        font-family: "Public Sans", sans-serif;
        font-size: 12px;
        text-decoration: none;
    }

    .about-me-container{
        margin-top: 6rem;
    }

    .about-me-container-text {
        padding-block: 2rem 2.4375rem;
        border-top: 1px solid #979797;
        border-bottom: 1px solid #979797;
        margin-top: 2rem;
    }

    .about-me-container p {
        line-height: 1.875rem;
        margin-top: 1.75rem;
    }

    @media only screen and (min-width: 768px){
        picture{
            position: relative;
        }

        .hero-heading{
            position: absolute;
            margin-top: -14.5rem;
            width: 514px;
            z-index: 1000;
            background-color: #FAFAFA;
        }

        .about-me-container{
            display: flex;
            gap: 4.3125rem;
        }

        .about-me-container-text{
            flex: 1;
            margin-top: 0;
        }

        picture{
            height: 100%;
        }
    }

    @media only screen and (min-width: 1100px){
        .container{
            width: 1015px;
        }
    }
</style>