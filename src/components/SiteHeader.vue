<template>
    <div class="navbar">
        <div class="header-container">
            <img class="site-logo" src="/src/assets/eye-and-the-needle.png" />
            <h1 class="header">N. ALEX STIFF</h1>
        </div>
        <div class="navlinks-container">
            <a class="navlink" href="/index.html">work</a>
            <a class="navlink" href="/contact.html">contact</a>
        </div>
    </div>
</template>

<style scoped>
.navbar {
    padding: 20px;
    display: grid;
    gap: 20px;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
}

.site-logo {
    width: 5.5vw;
    height: 5.5vw;
    margin-right: 16px;
}

.header-container {
    grid-column-end: span 2;
    display: flex;
    flex-direction: row;
    align-items: center;
}

.header {
    font-family: Oswald;
    font-weight: 700;
    font-size: 5.5vw;
    line-height: 5.5vw;
    margin: 0;
    padding: 0;
}

.navlinks-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: auto;
    gap: 0;
}

.navlink {
    display: block;
    align-self: self-end;
}

@media only screen and (min-width: 1440px) {
    .header {
        font-size: 86px;
        line-height: 86px;
    }
    .site-logo {
        width: 86px;
        height: 86px;
    }
}

@media only screen and (max-width: 766px) {
    .navbar {
        grid-template-columns: 1fr;
        grid-template-rows: auto auto;
    }
    .header-container {
        grid-column-end: span 1;
    }
    .header {
        font-size: 48px;
        line-height: 48px;
    }
    .site-logo {
        width: 48px;
        height: 48px;
    }
    .navlinks-container {
        gap: 20px;
    }
}

@media only screen and (max-width: 477px) {
    .header {
        font-size: 36px;
        line-height: 36px;
    }
    .site-logo {
        display: none;
    }
    .navlinks-container {
        grid-template-columns: 1fr;
        grid-template-rows: auto auto;
    }
}
</style>
