<script setup>

</script>

<template>    
    <section class="banner">
        <div class="container">
            <div class="banner-item">
                <h2 class="banner-item--title">Онлайн-сервис <br> доставки еды на&nbsp;дом</h2>
                <p class="banner-item--subtitle">Блюда из любимого ресторана привезет курьер в перчатках, маске
                            и с антисептиком</p>
            </div>
        </div>
    </section>
    <section class="products">
        <div class="container">
            <div class="products-header">
                        <h3 class="products-header--title">Рестораны</h3>
                        <input type="text" class="products-header--search"
                            placeholder="Поиск блюд и ресторанов" />
            </div>
            <div class="products-wrapper" id="rests-container">
                <router-link class="products-card" :to="`/rest?id=${rest.id}`" v-for="rest in restArray" :key="rest.id">
                    <div class="products-card__image">
                                <img :src="getUrl(rest.image)" alt="Изображение Пицца плюс" width="384"
                                    height="250">
                    </div>
                    <div class="products-card__desription">
                        <div class="products-card__desription--row">
                            <h4 class="products-card__desription--title">{{ rest.title }}</h4>
                            <div class="products-card__desription--bage">
                               {{ rest.time }} мин
                            </div>
                        </div>
                    
                        <div class="products-card__desription-info">
                            <div class="products-card__desription-info--reiting">
                                        <svg width="15" height="15" viewBox="0 0 15 15" fill="none"
                                            xmlns="http://www.w3.org/2000/svg">
                                            <path
                                                d="M14.6515 6.24221C14.5553 5.94476 14.2915 5.73349 13.9793 5.70536L9.73947 5.32038L8.06292 1.39623C7.9393 1.10864 7.65776 0.922485 7.34495 0.922485C7.03215 0.922485 6.75061 1.10864 6.62699 1.39691L4.95043 5.32038L0.709893 5.70536C0.398319 5.73417 0.135163 5.94476 0.0384405 6.24221C-0.0582818 6.53966 0.0310434 6.86592 0.266741 7.07158L3.47158 9.88224L2.52655 14.0451C2.45739 14.3512 2.5762 14.6676 2.83016 14.8512C2.96667 14.9498 3.12638 15 3.28744 15C3.4263 15 3.56404 14.9626 3.68766 14.8886L7.34495 12.7028L11.0009 14.8886C11.2684 15.0495 11.6057 15.0349 11.8591 14.8512C12.1131 14.667 12.2318 14.3505 12.1627 14.0451L11.2177 9.88224L14.4225 7.07214C14.6582 6.86592 14.7482 6.54022 14.6515 6.24221Z"
                                                fill="#FFC107" />
                                        </svg>
                                       {{ rest.rating }}
                            </div>
                            <div class="products-card__desription-info--price">От {{ rest.price }} ₽</div>
                            <div class="products-card__desription-info--group">{{ rest.type }} </div>
                        </div>
                    </div>
                </router-link>
            </div>
        </div>
    </section>    
</template>

<script setup>
import {restArray} from '../constants/rest'
 const getUrl = (name) => {
    return new URL(`../assets/images/restaurant/${name}`, import.meta.url)
 }
</script>

<style scoped></style>
