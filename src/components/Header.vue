<template>
   <header class="header">
            <div class="container">
                <div class="header-box">
                    <router-link class="header-logo logo" to="/">
                        <img class="logo-image" src="../assets/images/logo.png" alt="logo" width="100" height="36">
                    </router-link>
                    <div class="header-controls">
                        <button class="btn btn-primary">
                           <img src="../assets/images/person.svg" alt="Иконка Войти">
                            Войти
                        </button>
                        <button class="btn btn-outline" @click="openModal()">
                           <img src="../assets/images/basket.svg" alt="Иконка Корзина">
                            Корзина
                        </button>
                    </div>
                </div>
            </div>
        </header>
</template>

<script setup>
 const emit = defineEmits(['toggleModal'])
 const openModal = () =>  emit('toggleModal')
</script>

<style scoped>
.header {
    min-height: 124px;
    display: flex;
    align-items: center;
}

.header-box {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.header-controls {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    gap: 10px;
}
</style>