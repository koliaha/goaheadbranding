<template>
    <h1 class="text-title">Цвет</h1>
    <p class="text-prime  title__text design-logo-wrapper">У каждого юнита есть своя цветовая палитра, которая состоит
        из основного и дополнительного цветов.</p>
    <h3 class="text-prime mb-40"><b>Основной цвет помогает добиться узнаваемости юнита</b></h3>
    <div class="color-main-list">
        <div class="color-main-left">
            <div class="color-item__item color-item__item-wide">
                <div class="color-item__box" :style="{ 'backgroundColor': `#${colorMain[0].hex}` }"></div>
                <div class="color-item__title text-prime">{{ colorMain[0].name }}</div>
                <div class="color-item__descriptions">
                    <p><b>RGB</b> <span>{{ roRgb(colorMain[0].hex) || 0 }}</span> </p>
                    <p><b>CMYK</b> <span>{{ colorMain[0].cmyk || 0 }}</span> </p>
                    <p><b>HEX</b> <span>{{ colorMain[0].hex || 0 }}</span> </p>
                </div>
            </div>
        </div>
        <div class="color-item-list color-main-right">
            <div class="color-item__item color-item__item-wide" v-for="(i, index) in colorMain.slice(1)" :key="index">
                <div class="color-item__box" :style="{ 'backgroundColor': `#${i.hex}` }"></div>
                <div class="color-item__title">{{ i.name }}</div>
                <div class="color-item__descriptions">
                    <p><b>RGB</b> <span>{{ roRgb(i.hex) || 0 }}</span> </p>
                    <p><b>CMYK</b> <span>{{ i.cmyk || 0 }}</span> </p>
                    <p><b>HEX</b> <span>{{ i.hex || 0 }}</span> </p>
                </div>
            </div>
        </div>
    </div>

    <h3 class="text-prime mb-40"><b>Дополнительные помогают при создании инфографики</b></h3>
    <div class="color-list">
        <div class="color-item" v-for="(i, index) in colorList" :key="index">
            <div class="color-item-title">
                {{ i.name }}
            </div>
            <div class="color-item-list">
                <div class="color-item__item" v-for="(j, jetix) in i.list" :key="jetix">
                    <div class="color-item__box" :style="{ 'backgroundColor': `#${j.hex}` }"></div>
                    <div class="color-item__descriptions">
                        <p><b>RGB</b> <span>{{ roRgb(j.hex) }}</span> </p>
                        <p><b>CMYK</b> <span>{{ j.cmyk }}</span> </p>
                        <p><b>HEX</b> <span>{{ j.hex }}</span> </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <h3 class="text-prime mb-40"><b>Как используем</b></h3>
    <ul class="design-color-list-uses text-prime">
        <li>Если говорим от лица Go Ahead, то используем оранжевый цвет Go Ahead.
        </li>
        <li>Если говорим от лица Go Ahead и одного из юнитов, то основным цветом становится оранжевый Go Ahead, а
            дополнительным — цвет юнита.</li>
        <li>Если говорим от лица юнита, то используем цвет юнита.</li>
    </ul>
    <div class="design-color-link">
        <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=519-7525&t=rg3F4jofo6ggK1vf-0"
            target="_blank" class="btn text-prime">Гайд по цветам</a>
    </div>
</template>
<script>
import { color_list, color_main } from '@/datas/colors'
export default {
    computed: {
        colorList() {
            return color_list
        },
        colorMain() {
            return color_main
        }
    },
    methods: {
        roRgb(str) {
            let aRgbHex = str.match(/.{1,2}/g);
            let aRgb = [
                parseInt(aRgbHex[0], 16),
                parseInt(aRgbHex[1], 16),
                parseInt(aRgbHex[2], 16)
            ];
            return aRgb.join(' ')
        },

    },
}
</script>
<style lang="scss">
@use "@/assets/scss/abstracts" as *;

.color-list {
    @include flex(row, space-between, center);
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 80px;
}

.color-item {
    max-width: 608px;
    width: 100%;

    &-title {
        font-weight: 600;
        margin-bottom: 12px;
    }

    &__title {
        font-weight: 600;
        font-size: 13px;
        line-height: 17px;
        margin: 8px 0;
    }

    &-list {
        @include flex(row, start, center);
        gap: 4px;
    }

    &__item {
        max-width: 98px;
        width: 100%;

        &-wide {
            max-width: 102px;
        }
        &-border{
            border: 1px solid $black;
        }
    }

    &__box {
        height: 50px;
        background: $black;
        margin-bottom: 6px;
        cursor: pointer;
        transition: 0.3s opacity;

        &:hover {
            opacity: 0.8;
        }
        &.no-hover{
            &:hover {
            opacity: 1;
        }
        }
    }

    &__descriptions {
        font-weight: 400;
        font-size: 10px;
        line-height: 12px;

        p {
            margin-bottom: 5px;
        }

        span {
            margin-left: 4px;
        }
    }
}

.design-color {
    &-list-uses {
        margin-bottom: 100px;
    }

    &-link {
        @include flex(row, center, center);
    }
}

.color-main-list {
    @include flex(row, start);
    margin-bottom: 100px;
    gap: 67px;
}

.color-main-left {
    max-width: 247px;
    width: 100%;

    .color-item__item {
        max-width: 100%;
        width: 100%;

        .color-item__box {
            height: 150px;
        }

        .color-item__title {
            font-size: 24px;
            line-height: 29px;
        }
    }
}

.color-main-right {
    gap: 16px;
    width: 100%;
}
</style>
