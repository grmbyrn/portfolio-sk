<script lang="ts">
    let isMenuOpen: boolean = false

    const toggleMenu = () => {
        isMenuOpen = !isMenuOpen
    }
</script>

<header>
    <a href="/">
        <img src="/images/logo.svg" alt="logo">
    </a>
    {#if !isMenuOpen}
        <button on:click={toggleMenu} class="open">
            <img src="/images/icons/hamburger.svg" alt="">
        </button>
    {:else}
        <button on:click={toggleMenu} class="close">
            <img src="/images/icons/close.svg" alt="">
        </button>
    {/if}

    {#if isMenuOpen}
        <div class="modal">
            <ul class="nav-list">
                <li>
                    <a href="/" on:click={toggleMenu}>Home</a>
                </li>
                <li>
                    <a href="/portfolio" on:click={toggleMenu}>Portfolio</a>
                </li>
                <li>
                    <a href="/contact" on:click={toggleMenu}>Contact Me</a>
                </li>
            </ul>
        </div>
    {/if}
</header>

<style>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 2rem 2rem 0 2rem;
    }

    button{
        background-color: transparent;
        border: none;
        cursor: pointer;
    }

    .close{
        z-index: 1000;
    }

    .modal{
        position: fixed;
        top: 5.5rem;
        left: 0;
        width: 100%;
        height: 100%;
        background: #33323D;
		z-index: 999;
		display: flex;
		align-items: flex-start; /* Center vertically */
		justify-content: center;
    }

    .nav-list {
		display: flex;
		flex-direction: column;
		text-align: center; /* Center text */
        padding: 0;
		padding-top: 40px;
		margin: 0;
		list-style: none;
	}

    .nav-list li {
		font-size: 1.25rem;
		padding-block: 1.5rem;
	}

    .nav-list li a {
		text-decoration: none;
		color: #333D4B;
        font-size: 1.5rem;
        font-weight: 800;
        line-height: 2rem;
        color: #ffffff;
	}
</style>