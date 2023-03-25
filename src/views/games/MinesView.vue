<script>
export default {
    data() {
        return {
            loader: false,
        }
    }
}
</script>

<template>
    <section id="background-image-home">
        <section id="background-home">
            <figure id="logo-home">
                <img src="@/assets/img/logo-ninja-1.png" alt="">
            </figure>

            <section v-if="!loader" id="quantitys-mines">
                <p>Quantidade de mines: <span>5</span></p>
            </section>

            <section v-if="!loader" id="mines">
                <section class="line">
                    <article class="icon-line">
                        💣
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                </section>
                <section class="line">
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💣
                    </article>
                </section>
                <section class="line">
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💣
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                </section>
                <section class="line">
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                </section>
                <section class="line">
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💣
                    </article>
                    <article class="icon-line">
                        💣
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                    <article class="icon-line">
                        💎
                    </article>
                </section>
            </section>

            <section v-if="loader" id="loader">
                <article id="loader-bg">

                </article>
            </section>

            <footer id="game-name">
                <p>Você está jogando Mines!</p>
            </footer>
        </section>
    </section>
</template>

<style>
#background-home {
    width: 100%;
    background: rgba(20, 20, 20, 0.959);
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

#background-image-home {
    width: 100%;
    height: 100%;
    background-image: url('@/assets/img/hack.gif');
    background-repeat: no-repeat;
    background-size: cover;
}

#logo-home img {
    width: 100px;
    margin-bottom: 50px;
}

#quantitys-mines p {
    font-size: 18px;
    color: #27A792;
    font-family: 'Nunito';
    font-weight: bold;
}

#quantitys-mines span {
    color: white;
}

#mines {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 30px;
}

.line {
    display: flex;
    flex-direction: row;
}

.icon-line {
    font-size: 23px;
    padding: 5px;
    background: rgb(39, 39, 39);
    border: 1px solid;
}

#game-name {
    width: 100%;
    text-align: center;
    font-size: 18px;
    color: white;
    font-family: 'Nunito';
    font-weight: bold;
    position: absolute;
    bottom: 20px;
}

#loader {
    height: 260px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}

#loader-bg {
    width: 150px;
    height: 150px;
    border-radius: 100%;
    border: 2px solid transparent;
    border-left: 2px solid #27A792;
    animation-name: loader;
    animation-duration: 0.7s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
}

@keyframes loader {
    to {
        transform: rotate(360deg);
    }
}
</style>