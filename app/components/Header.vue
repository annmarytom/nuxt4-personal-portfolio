<template>
    <div class="header">
        <div class="header-inner">
            <div class="header-inner_logo">
                <a href="https://preview.colorlib.com/#personal"> <img :src="logo" /></a>
            </div>
            <div class="header-inner_navigation">
                <ul class="header-inner_navigation--list">
                    <li>
                        <NuxtLink to="/" class="header-inner_listitems">HOME</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/about" class="header-inner_listitems">ABOUT</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/services" class="header-inner_listitems">SERVICES</NuxtLink>
                    </li>
                    <li class="header-inner_listitems">PORTFOLIO</li>
                    <li class="header-inner_listitems">BLOG</li>
                    <li class="header-inner_listitems">PAGES</li>

                    <li class="header-inner_listitems">PRICING</li>
                    <li>
                        <NuxtLink to="/contacts" class="header-inner_listitems">CONTACT</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script setup>
const logo = ref("https://preview.colorlib.com/theme/personal/img/logo.png");

</script>


<style lang="scss">
$header_bg: #ffffff;
$header_color: black;

.header {

    width: 100%;
    height: 60px;
    background-color: $header_bg;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

.header-inner {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 10px 20px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 20px;


    &_logo img {
        max-height: 40px;
        object-fit: contain;

        &:hover {
            cursor: pointer;
        }
    }

    .header-inner_navigation--list {
        list-style: none;
        display: flex;
        gap: 30px;
        padding: 0;
        margin: 0;
    }

    &_listitems {
        font-size: 12px;

        font-family: sans-serif;
        font-weight: 600;
        color: $header_color;
        cursor: pointer;
        transition: color 0.3s ease;

        &:hover {
            color: #007BFF;
        }
    }

    @media (max-width: 768px) {
        .header-inner {
            flex-direction: column;
            gap: 10px;
        }

        .header-inner_navigation--list {
            flex-direction: column;
            gap: 10px;
        }
    }
}
</style>
