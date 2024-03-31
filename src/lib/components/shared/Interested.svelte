<script lang="ts">
    import Button from "./Button.svelte";
</script>

<div class="interested-container">
    <h2>Interested in doing a project together?</h2>
    <div class="line">
        <hr>
    </div>
    <div class="btn">
        <Button
            link={'/contact-me'}
            text={'Contact Me'}
        />
    </div>
</div>

<style>
    .interested-container{
        margin-top: 5rem;
    }
    
    h2{
        font-size: 2.5rem;
        text-align: center;
        line-height: 42px;
        letter-spacing: -0.36px;
    }

    .line{
        display: none;
    }

    .btn{
        display: flex;
        justify-content: center;
        margin-top: 2.5rem;
    }

    @media only screen and (min-width: 768px){
        .interested-container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 6rem;
            padding-inline: 2rem;
        }

        h2{
            text-align: left;
            flex: 3;
        }

        .line{
            display: block;
            width: 113px;
            flex: 1;
            margin-top: 2rem;
            padding-inline: 1rem;
        }

        .btn{
            width: 11rem;
            flex: 2;
            justify-content: flex-end;
            margin-top: 0rem;
        }
    }
</style>