<script lang="ts">
    export let previousProject: string
    export let nextProject: string
</script>

<div class="scroll-projects-container">
    <div class="previous-project">
        <div class="arrow previous-project-arrow">
            <a href={previousProject}>
                <img src="/images/icons/arrow-left.svg" alt="arrow left">
            </a>
        </div>
        <div class="previous-project-text">
            <h2>{previousProject.slice(1, 2).toUpperCase() + previousProject.slice(2).toLowerCase()}</h2>
            <p>Previous Project</p>
        </div>
    </div>
    <div class="next-project">
        <div class="arrow next-project-arrow">
            <a href={nextProject}>
                <img src="/images/icons/arrow-right.svg" alt="arrow right">
            </a>
        </div>
        <div class="next-project-text">
            <h2>{nextProject.slice(1, 2).toUpperCase() + nextProject.slice(2).toLowerCase()}</h2>
            <p>Next Project</p>
        </div>
    </div>
</div>

<style>
    .scroll-projects-container{
        display: flex;
        justify-content: space-between;
        margin-top: 4rem;
        border-top: 1px solid #979797;
        border-bottom: 1px solid #979797;
    }

    .scroll-projects-container h2{
        font-size: 2rem;
        letter-spacing: -0.29px;
        line-height: 36px;
    }

    .arrow{
        margin-top: 1.5rem;
    }

    .previous-project{
        border-right: 1px solid #979797;
        flex: 1;
        padding-bottom: 1.5rem;
    }

    .next-project{
        flex: 1;
        text-align: right;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: flex-end;
        padding-bottom: 1.5rem;
    }
</style>