<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            sidebar: false
        }
    },
}
</script>

<template>
    <header>
        <section @click="sidebar = true" id="icon-open">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
        </section>

        <nav id="nav-header" v-if="sidebar">
            <figure id="logo-header">
                <img src="@/assets/img/logo-ninja-1.png" alt="Ninja Pro - APP">
            </figure>

            <section @click="sidebar = false" id="close">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M10.5 19.5L3 12m0 0l7.5-7.5M3 12h18" />
                </svg>
            </section>

            <section id="links-nav">
                <router-link to="/" @click="sidebar = false" class="link-nav border-top-1">
                    <figure class="icon-link-nav">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25" />
                        </svg>
                    </figure>

                    <span class="title-link-nav">Home</span>
                </router-link>

                <a href="https://instagram.com/ninjaviatiorpro?igshid=ZDdkNTZiNTM=" class="link-nav border-top-1" target="_blank">
                    <figure class="icon-link-nav">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M6 12L3.269 3.126A59.768 59.768 0 0121.485 12 59.77 59.77 0 013.27 20.876L5.999 12zm0 0h7.5" />
                        </svg>
                    </figure>

                    <span class="title-link-nav">Entre em contato</span>
                </a>

                <a href="https://instagram.com/ninjaviatiorpro?igshid=ZDdkNTZiNTM=" class="link-nav border-top-1" target="_blank">
                    <figure class="icon-link-nav">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" d="M15.75 10.5l4.72-4.72a.75.75 0 011.28.53v11.38a.75.75 0 01-1.28.53l-4.72-4.72M4.5 18.75h9a2.25 2.25 0 002.25-2.25v-9a2.25 2.25 0 00-2.25-2.25h-9A2.25 2.25 0 002.25 7.5v9a2.25 2.25 0 002.25 2.25z" />
                        </svg>
                    </figure>

                    <span class="title-link-nav">Tutoriais</span>
                </a>

                <article @click="redirectToWebPage('https://go.aff.betpix365.com/cit9oufh?utm_source=app')" id="yellow-link-nav" class="link-nav">
                    <figure class="icon-link-nav">
                        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
                            <path stroke-linecap="round" stroke-linejoin="round" d="M11.48 3.499a.562.562 0 011.04 0l2.125 5.111a.563.563 0 00.475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 00-.182.557l1.285 5.385a.562.562 0 01-.84.61l-4.725-2.885a.563.563 0 00-.586 0L6.982 20.54a.562.562 0 01-.84-.61l1.285-5.386a.562.562 0 00-.182-.557l-4.204-3.602a.563.563 0 01.321-.988l5.518-.442a.563.563 0 00.475-.345L11.48 3.5z" />
                        </svg>
                    </figure>

                    <span class="title-link-nav">Cadastre-se e ganhe R$350,00</span>
                </article>
            </section>
        </nav>
    </header>
</template>

<style scoped>
#icon-open {
    width: 40px;
    padding: 10px 0px 0px 10px;
    cursor: pointer;
    position: absolute;
    z-index: 1;
    color: #27A792;
}

#nav-header {
    width: 85%;
    position: absolute;
    z-index: 10;
    height: 100%;
    background: rgb(23, 23, 23);
}

#logo-header {
    width: 100%;
    display: flex;
    align-items: center;
    margin-top: 20px;
}

#logo-header img {
    width: 100px;
    margin: 10px auto;
}

#close {
    position: absolute;
    top: 12px;
    left: 12px;
    width: 20px;
    color: #27A792;
}

#links-nav {
    width: 100%;
    height: auto;
    margin-top: 30px;
}

.link-nav {
    width: 100%;
    height: 60px;
    transition: 0.2s;
    display: flex;
    flex-direction: row;
    align-items: center;
    cursor: pointer;
}

.link-nav:hover {
    background: #272727;
    transition: 0.2s;
}

.icon-link-nav {
    width: 20px;
    color: #27A792;
    margin-left: 16px;
}

.title-link-nav {
    font-family: 'Montserrat';
    font-size: 18px;
    margin-left: 20px;
    color: #27A792;
}

.border-top-1 {
    border-top: 1px solid #272727;
}

.border-bottom-1 {
    border-bottom: 1px solid #272727;
    transition: 0.2s;
}

#yellow-link-nav {
    background: #e6b027;
    transition: 0.2s;
}

#yellow-link-nav:hover {
    background: #d9a319;
}

#yellow-link-nav .icon-link-nav,
#yellow-link-nav .title-link-nav {
    color: white;
}
</style>