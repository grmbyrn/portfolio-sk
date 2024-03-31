<script lang="ts">
	import Button from "../shared/Button.svelte";

    export let index: number
    export let bgImageMobile: string
    export let bgImageTablet: string
    export let bgImageDesktop: string
    export let title: string
    export let description: string
    export let link: string
</script>

<div class:active={index % 2 == 0} class="container">
    <picture>
        <source media="(min-width: 1100px)" srcset={bgImageDesktop}>
        <source media="(min-width: 768px)" srcset={bgImageTablet}>
        <img src={bgImageMobile} alt="hero">
    </picture>
    <div class="text-container">
        <h2>{title}</h2>
        <p>{description}</p>
        <Button
            link={link}
            text={'View Project'}
        />
    </div>
</div>

<style>
    .text-container{
        padding-block: 1.5rem;
        border-top: 1px solid #979797;
        border-bottom: 1px solid #979797;
        margin-top: 2rem;
        margin-bottom: 4.5rem;
        color: #33323D;
    }

    h2{
        font-size: 2.5rem;
        letter-spacing: -0.36px;
        line-height: 42px;
        margin: 0;
    }

    p {
        font-size: 15px;
        line-height: 30px;
    }

    @media only screen and (min-width: 768px){
        .container{
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 4.375rem;
            margin-top: 5rem;
        }

        .active {
            display: flex;
            flex-direction: row-reverse;
        }

        picture{
            flex: 1;
        }

        .text-container{
            padding-block: 2.5rem;
            flex: 1;
            margin-top: 0rem;
            margin-bottom: 0rem;
        }
    }
</style>