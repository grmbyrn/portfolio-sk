<footer>
    <div class="footer-left">
        <a href="/">
            <img src="/images/logo.svg" class="filter" alt="logo">
        </a>
        <ul class="nav-list">
            <li>
                <a href="/">Home</a>
            </li>
            <li>
                <a href="/portfolio">Portfolio</a>
            </li>
            <li>
                <a href="/contact">Contact Me</a>
            </li>
        </ul>
    </div>
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
</footer>

<style>
    footer{
        background-color: #33323D;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding-block: 3.5rem;
        margin-top: 5rem;
    }

    .filter{
        filter: invert(100%) sepia(100%) saturate(0%) hue-rotate(254deg) brightness(106%) contrast(101%);
        margin: 0 auto;
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

    .nav-list{
        display: flex;
        flex-direction: column;
        gap: 2rem;
        margin-top: 2.5rem;
    }

    .social-media{
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 1rem;
        margin-top: 2.5rem;
    }

    @media only screen and (min-width: 768px){
        footer{
            flex-direction: row;
            align-items: center;
            justify-content: space-between;
            padding-inline: 2.5rem;
        }

        .footer-left{
            display: flex;
            gap: 3rem;
        }

        .nav-list{
            flex-direction: row;
            margin-top: 0rem;
            gap: 2.625rem;
        }

        .social-media{
            margin-top: 0rem;
        }
    }

    @media only screen and (min-width: 1100px){
    }
</style>