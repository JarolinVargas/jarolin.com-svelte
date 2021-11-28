<script>
    import githubIcon from '../assets/icons/github-brands.svg'
</script>

<article>
    <h1 class="my-name aboutme-gradient" style="opacity: 1; transform: none;">Jarolin E. Vargas</h1>
    <h3 class="aboutme-gradient">Front-End Engineer & UI/UX Designer</h3>
    <p class="my-bio" style="opacity: 1; transform: none;">Hey! I’m a Front-End Engineer with some UI &amp; UX design skills who strives to deliver the best experience possible for the end-user. I have experience building full-scale web applications both independently, and as part of a team. While I specialize in user-facing features, I sometimes dive into the back-end with PHP and MySQL. Check out the rest of my portfolio and hit me up if you’re interested in working together. ✌</p>
    <ul class="icons">
        <li><a href="#"><img src={githubIcon} alt="github"/></a></li>
        <li><a href="#"><img src={githubIcon} alt="dribbble"/></a></li>
        <li><a href="#"><img src={githubIcon} alt="linkedin"/></a></li>
        <li><a href="#"><img src={githubIcon} alt="resume"/></a></li>
    </ul>
</article>

<style>
    article {
        width: auto;
        align-self: center;
        grid-column-start: 2;
        margin: 30px;
        margin-left: 0px;
    }

    h1 {
        font-family: "Poppins",sans-serif;
        font-size: 1.88em;
        font-weight: 600;
        margin-top: 0;
        margin-bottom: 5px;
    }

    h3 {
        margin: 0;
        line-height: 1.2;
        font-weight: 500;
    }

    p {
        line-height: 2.3;
        font-size: .95em;
        color: #FFF;
        margin: 25px 0px;
    }

    .icons {
        padding: 0;
        z-index: 1;
        position: relative;
    }

    .icons li {
        display: inline-block;
        margin-right: 30px;
    }

    .icons img {
        width: 1em;
    }
</style>