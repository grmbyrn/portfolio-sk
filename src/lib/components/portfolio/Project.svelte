<script lang="ts">
	import Button from "../shared/Button.svelte";
	import Scroll from "./Scroll.svelte";

    export let heroMobile: string
    export let heroTablet: string
    export let heroDesktop: string
    export let title: string
    export let desc: string
    export let tags: string[]
    export let link: string
    export let background: string
    export let staticPreviewMobile1: string
    export let staticPreviewTablet1: string
    export let staticPreviewDesktop1: string
    export let staticPreviewMobile2: string
    export let staticPreviewTablet2: string
    export let staticPreviewDesktop2: string
    export let previousProject: string
    export let nextProject: string
</script>

<div class="container">
    <picture>
        <source media="(min-width: 1100px)" srcset={heroDesktop}>
        <source media="(min-width: 768px)" srcset={heroTablet}>
        <img src={heroMobile} alt="hero">
    </picture>
    <div class="flex-container">
        <div class="description-container">
            <h1>{title}</h1>
            <p>{desc}</p>
            <div class="tags-container">
                {#each tags as tag, index}
                    <span>{tag}{index !== tags.length - 1 ? ' / ' : ''}</span>
                {/each}
            </div>
            <div class="btn">
                <Button
                    link={link}
                    text={'View Website'}
                />
            </div>
    </div>
        <div class="background-container">
            <h2>Project Background</h2>
            <p>{background}</p>
            <h2>Static Previews</h2>
            <picture>
                <source media="(min-width: 1100px)" srcset={staticPreviewDesktop1}>
                <source media="(min-width: 768px)" srcset={staticPreviewTablet1}>
                <img src={staticPreviewMobile1} alt="hero">
            </picture>
            <picture>
                <source media="(min-width: 1100px)" srcset={staticPreviewDesktop2}>
                <source media="(min-width: 768px)" srcset={staticPreviewTablet2}>
                <img src={staticPreviewMobile2} alt="hero">
            </picture>
        </div>
    </div>
    <Scroll
        previousProject={previousProject}
        nextProject={nextProject}
    />
</div>

<style>
    .container{
        padding-inline: 2rem;
    }

    picture{
        margin-top: 2.5rem;
    }

    picture img{
        width: 100%;
        object-fit: cover;
    }

    .description-container{
        padding-block: 1.5rem;
        border-top: 1px solid #979797;
        border-bottom: 1px solid #979797;
        margin-top: 2.5rem;
    }

    .description-container h1 {
        font-size: 2.5rem;
        letter-spacing: -0.36px;
        line-height: 42px;
    }

    .description-container p,
    .background-container p {
        line-height: 30px;
    }

    .tags-container{
        color: #5FB4A2;
        font-size: 13px;
        line-height: 30px;
        margin-top: 2rem;
    }

    .background-container{
        margin-top: 3rem;
    }

    .background-container h2 {
        font-size: 2rem;
        letter-spacing: -0.29px;
        line-height: 42px;
    }

    @media only screen and (min-width: 768px){
        .description-container{
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            grid-template-rows: repeat(3, 1fr);
            grid-column-gap: 12px;
            grid-row-gap: 0px;
        }

        .description-container h1 {
            grid-area: 1 / 1 / 2 / 3;
        }

        .tags-container{
            grid-area: 2 / 1 / 3 / 3;
            margin-top: 1rem;
        }

        .btn{
            grid-area: 3 / 1 / 4 / 3;
        }

        .description-container p {
            grid-area: 1 / 3 / 4 / 5;
        }
    }
</style>