<svelte:head>
    <link href="https://fonts.googleapis.com/css?family=Poppins:400,500,600&display=swap" rel="stylesheet" />
</svelte:head>

<script>
    import '../frame.css';
</script>

<div class="root">
    <div class="frame">
        <nav>
            <div class="active-tab-indicator"></div>
            <ul class="nav-desktop">
                <li class="navitem-separator"></li>
                <li><a href="/">About Me</a></li>
                <li class="navitem-separator"></li>
                <li><a href="/portfolio">Portfolio</a></li>
                <li class="navitem-separator"></li>
                <li><a href="/writings">Writings</a></li>
                <li class="navitem-separator"></li>
                <li><a href="/contact">Contact</a></li>
                <li class="navitem-separator"></li>
            </ul>
        </nav>
        <main class="content">
            <slot/>
        </main>
    </div>
</div>

<style>
    .root {
        height: 100vh;
        width: 100vw;
        display: flex;
        vertical-align: middle;
        background-image: url('../src/assets/diagonal-line.svg');
        position: fixed;
        top: 0;
        left: 0;
    }

    .frame {
        width: 1300px;
        height: 725px;
        max-width: 100%;
        max-height: 100%;
        margin: auto;
        padding: 30px 15px;
        font-size: 16px;
        color: rgba(45,51,86,.7490196078431373);
        position: relative;
        box-sizing: border-box;
    }

    main {
        width: 100%;
        height: 100%;
        border: 1px solid;
        border-image-slice: 1;
        border-top: 0;
        z-index: 1;
        position: relative;
        box-sizing: border-box;
        border-image-source: linear-gradient(to right, rgb(58, 244, 245), rgb(22, 77, 254));
        overflow: hidden;
    }

    nav {
        width: 100%;
        height: 50px;
        width: calc(100% - 30px);
        position: absolute;
        margin-top: -26px;
        display: flex;
        z-index: 2;
        font-size: 1.05em;
        -webkit-user-select: none;
        -ms-user-select: none;
        user-select: none;
    }

    .nav-desktop {
        display: flex;
        width: 100%;
        margin: 0;
        padding: 0;
        list-style: none;
        overflow: hidden;
    }

    li {
        display: inline-block;
        align-self: center;
        text-align: center;
        white-space: nowrap;
        font-weight: 500;
    }

    li:not(.navitem-separator) {
        padding: 0 10px;
        width: -webkit-fit-content;
        width: -moz-fit-content;
        width: fit-content;
    }

    a {
        text-transform: uppercase;
        color: #FFF;
    }

    .navitem-separator {
        height: 1px;
        flex-basis: 30px;
        min-width: 30px;
        margin-top: 1px;
        background-image: linear-gradient(to right, rgb(58, 244, 245), rgb(22, 77, 254));
        background-attachment: fixed;
        mix-blend-mode: difference;
    }

    .navitem-separator:last-child {
        flex-basis: 100%;
    }
    
    .active-tab-indicator {
        left: 85px;
        background-image: linear-gradient(to right, rgb(58, 244, 245), rgb(22, 77, 254));
        width: 6px;
        height: 6px;
        border-radius: 100%;
        background-attachment: fixed;
        mix-blend-mode: difference;
        position: absolute;
        transition-property: left;
        transition-duration: .3s;
        transition-timing-function: ease-out;
    }

    @media screen and (max-width: 940px) {
        .root {
            position: relative;
        }

        .frame {
            padding-top: 0;
            max-height: none;
        }

        main {
            height: fit-content;
        }

        nav {
            margin-top: 0;
        }

        .nav-desktop {
            position: fixed;
            border-bottom: solid 1px;
            border-image-source: linear-gradient(to right, rgb(58, 244, 245), rgb(22, 77, 254));
            border-image-slice: 1;
            height: 50px;
            width: calc(100vw - 30px);
            background-image: linear-gradient(to right, rgb(58 244 245 / 44%), rgb(22 77 254 / 37%));
            backdrop-filter: blur(10px);
        }

        .active-tab-indicator {
            display: none;
        }

        .nav-desktop li:first-child {
            flex-basis: 100%;
        }
    }

    @media screen and (max-width: 600px) {
        nav {
           font-size: 13px; 
        }

        .navitem-separator {
            min-width: 10px;
        }

        li:not(.navitem-separator) {
            padding: 0 5px;
        }
    }

    @media screen and (max-width: 400px) {
        .frame {
            padding-left: 5px;
            padding-right: 5px;
        }

        nav {
            font-size: 12px;
        }

        .navitem-separator {
            min-width: 5px;
        }

        .nav-desktop {
            width: calc(100vw - 10px);
        }
    }
</style>