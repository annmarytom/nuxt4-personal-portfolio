<template>
    <section class="hero">
        <div class="hero__inner">

            <div class="hero__content">
                <p class="hero__kicker">{{ kicker }}</p>
                <h1 class="hero__name">{{ name }}</h1>
                <p class="hero__desc">{{ description }}</p>

                <a class="hero__btn" :href="ctaHref">
                    {{ ctaText }}
                </a>
            </div>


            <div class="hero__visual">

                <div class="hero__frame" aria-hidden="true">
                    <div class="hero__dots"></div>
                </div>


                <img class="hero__person" :src="imageSrc" :alt="imageAlt" />
            </div>
        </div>
    </section>
</template>

<script setup>
defineProps({
    kicker: { type: String, default: "THIS IS ME" },
    name: { type: String, default: "PHILIP GILBERT" },
    description: {
        type: String,
        default:
            "You will begin to realise why this exercise is called the Dickens Pattern with reference to the ghost showing Scrooge some different futures."
    },
    ctaText: { type: String, default: "DISCOVER NOW" },
    ctaHref: { type: String, default: "#" },


    imageSrc: { type: String, default: "/images/about-img.png" },
    imageAlt: { type: String, default: "Profile photo" }
})
</script>

<style lang="scss" scoped>
$bg: #f7f8ff;
$text: #111827;
$muted: #6b7280;
$primary: #6b7cff;
$primary2: #67b6ff;

.hero {
    background: $bg;
    padding: 90px 0;
    overflow: hidden;

    &__inner {
        width: min(1180px, calc(100% - 48px));
        margin: 0 auto;

        display: grid;
        grid-template-columns: 1.05fr 0.95fr;
        align-items: center;
        gap: 56px;
    }


    &__content {
        max-width: 520px;
    }

    &__kicker {
        margin: 0 0 16px;
        font-size: 12px;
        letter-spacing: 0.18em;
        font-weight: 700;
        color: $text;
    }

    &__name {
        margin: 0 0 18px;
        font-size: 64px;
        line-height: 1.05;
        font-weight: 900;
        letter-spacing: 0.02em;
        color: #222;
    }

    &__desc {
        margin: 0 0 26px;
        font-size: 14px;
        line-height: 1.8;
        color: $muted;
        max-width: 460px;
    }

    &__btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;

        height: 46px;
        padding: 0 28px;
        border-radius: 2px;
        text-decoration: none;
        font-weight: 800;
        font-size: 12px;
        letter-spacing: 0.05em;
        color: #fff;

        background: linear-gradient(90deg, $primary 0%, $primary2 100%);
        box-shadow: 0 12px 22px rgba(103, 182, 255, 0.25);
        transition: transform 0.15s ease, filter 0.15s ease;

        &:hover {
            transform: translateY(-1px);
            filter: brightness(1.02);
        }
    }

    &__visual {
        position: relative;
        min-height: 460px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    &__frame {
        position: absolute;
        width: 420px;
        height: 420px;
        right: 10px;
        top: 30px;
        border-radius: 4px;
        background: linear-gradient(90deg, $primary 0%, $primary2 100%);
        z-index: 1;
    }

    &__dots {
        position: absolute;
        inset: 16px;
        background: #f9fbff;
        border-radius: 3px;
        overflow: hidden;


        background-image: radial-gradient(rgba(107, 124, 255, 0.35) 2px, transparent 3px);
        background-size: 28px 28px;
    }

    &__person {
        position: relative;
        z-index: 2;
        width: 430px;
        max-width: 100%;
        height: auto;
        display: block;


        filter: drop-shadow(0 18px 30px rgba(0, 0, 0, 0.18));
    }
}

/* Responsive */
@media (max-width: 980px) {
    .hero {
        padding: 60px 0;

        &__inner {
            grid-template-columns: 1fr;
            text-align: center;
        }

        &__content {
            margin: 0 auto;
        }

        &__desc {
            margin-left: auto;
            margin-right: auto;
        }

        &__visual {
            min-height: 420px;
        }

        &__frame {
            right: 50%;
            transform: translateX(50%);
        }
    }
}

@media (max-width: 520px) {
    .hero__name {
        font-size: 44px;
    }

    .hero__frame {
        width: 320px;
        height: 320px;
        top: 20px;
    }

    .hero__person {
        width: 320px;
    }
}
</style>