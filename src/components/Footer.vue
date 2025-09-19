<template>
   <footer class="footer">
            <div class="container">
                <div class="footer-box">
                    <router-link class="footer-logo logo" to="/">
                        <img class="logo-image" src="../assets/images/logo.png" alt="logo" width="100" height="36">
                    </router-link>
                    <nav class="footer-nav">
                        <ul class="footer-nav__list">
                            <li>Ресторанам
                            </li>
                            <li>Курьерам
                            </li>
                            <li>Пресс-центр
                            </li>
                            <li>Контакты</li>
                        </ul>
                    </nav>
                    <div class="footer-social">
                        <img class="footer-social-image" src="../assets/images/social/insta.png" alt="insta" width="25"
                            height="25">
                        <img class="footer-social-image" src="../assets/images/social/fb.png" alt="fb" width="25" height="25">
                        <img class="footer-social-image" src="../assets/images/social/vk.png" alt="vk" width="25" height="25">
                    </div>
                </div>

            </div>
        </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
.footer {
    min-height: 156px;
    display: flex;
    align-items: center;
    padding: 60px 0;
}

.footer-box {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 36px;
    flex-wrap: wrap;
}

.footer-nav {
    flex-grow: 1;
}

.footer-nav__list {
    display: flex;
    list-style-type: none;
    align-items: center;
    gap: 15px;
    flex-wrap: wrap;
}

.footer-nav__list li {
    color: #595959;
    font-size: 18px;
}

.footer-social {
    display: flex;
    align-items: center;
    justify-content: flex-end;
    gap: 20px;
}
</style>