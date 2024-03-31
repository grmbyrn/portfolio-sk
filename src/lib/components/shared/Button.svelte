<script lang="ts">
    export let link: string
    export let text: string
</script>

<button>
    <a href={link}>{text}</a>
</button>

<style>
    button{
        margin-top: 1.5rem;
        font-family: "Public Sans", sans-serif;
        padding: 1rem 2rem;
        background-color: transparent;
        letter-spacing: 2px;
        border: 1px solid #33323D;
    }

    button a{
        color: #33323D;
        text-decoration: none;
    }

    @media only screen and (min-width: 768px){
        button{
            margin-top: 1rem;
        }
    }
</style>