<script>
export default {
  
}
</script>

<template>
    <section id="background-image-home">
        <section id="background-home">
            <figure id="logo-home">
                <img src="@/assets/img/logo-ninja-1.png" alt="">
            </figure>

            <h1 id="title-games">JOGOS DISPONÍVEIS</h1>

            <section class="button-game">
                <button class="disabled">
                    AVIATOR
                </button>
            </section>
            <section class="button-game">
                <button class="disabled">
                    DRAGON TIGER
                </button>
            </section>
            <section class="button-game">
                <button @click="this.$router.push('/mines')">
                    MINES
                </button>
            </section>
        </section>
    </section>
</template>

<style scoped>
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
    margin-bottom: 40px;
}

.button-game {
    margin-top: 15px;
}

.button-game button {
    width: 270px;
    height: 40px;
    background-image: linear-gradient(#80BEBF, #45B6A8);
    font-size: 15px;
    letter-spacing: 1.5px;
    font-weight: bold;
    border-radius: 10px;
    border: none;
    font-family: 'Nunito';
    cursor: pointer;
}

#title-games {
    margin-top: 50px;
    color: white;
    font-family: 'Nunito';
    font-size: 16px;
    letter-spacing: 1px;
    margin-bottom: 15px;
}

.disabled {
    background: gray !important;
    cursor: not-allowed !important;
}
</style>