<template>
    <footer class="footer">
        <ul class="footer__list">
            <li class="footer__item footer__item--logo">
                <img src="@/assets/images/logo.webp" alt="lumifilm logo" />
            </li>
            <li class="footer__item">
                <RouterLink to="/Cartelera">Cartelera</RouterLink>
            </li>
            <li class="footer__item">
                <RouterLink to="/Términos">Términos y Condiciones</RouterLink>
            </li>
            <li class="footer__item">
                <RouterLink to="/Políticas">Política de Privacidad</RouterLink>
            </li>
        </ul>
    </footer>
</template>


<script setup lang="ts"></script>


<style lang="scss" scoped>
@use '../assets/styles/variables' as *;
@use '../assets/styles/mixins' as *;
@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200..1000;1,200..1000&display=swap');

.footer {

    width: 100%;
    text-align: center;

    &__item {
        margin: 0 auto;
        @include regular-text(14px);

        a:hover {
            color: $red-color;
        }

        &--logo {
            width: 166px;
            height: 53px;
            display: flex;
            justify-content: center;

            img {
                max-width: 80%;
                margin: 0 auto;
            }
        }
    }

    &__social-list {
        display: flex;
        flex-direction: row;
        width: 40%;
        justify-content: space-evenly;
        margin: 0 auto;
        margin-bottom: 130px;
        padding-top: 20px;

    }

    &__social-item {
        :hover {
            @include image-hover-zoom(1.04, 0.3s);
        }

        img {
            width: 30px;
            height: 30px;
        }
    }
}

@media only screen and (min-width: 768px) {
    .footer {
        &__list {
            display: flex;
            flex-direction: row;
            max-width: 600px;
            margin: 0 auto;
            align-items: center;
        }

        &__social-list {
            max-width: 300px;
            margin-bottom: 40px;
        }
    }
}

@media only screen and (min-width: 1200px) {
    .hrFooter {
        max-width: 1200px;
    }
}
</style>
