<template>
    <h1 class="text-title">Логотип</h1>
    <p class="text-prime  title__text design-logo-wrapper " v-if="false">В основе формообразующего элемента логотипа лежит
        концепт про связь, единение, движение вперед, развитие. Лого напоминает кольца цепи, которые связывают все юниты
        воедино.</p>
    <h3 class="text-prime text-center mt-40"><b>Приоритетный вариант лого — цветной вертикальный</b></h3>
    <div class="design-logo--first-list">
        <div class="design-logo--first-item dark">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="first-item__img"> -->
            <div class="first-item__logo-title"><span>go</span>ahead</div>
        </div>
        <div class="design-logo--first-item ">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="first-item__img"> -->
            <div class="first-item__logo-title"><span>go</span>ahead</div>
        </div>
    </div>
    <h3 class="text-prime text-center"><b>Горизонтальная и черно-белая версии логотипа — второстепенные</b></h3>
    <div class="design-logo--second-list">
        
        
        <div class="design-logo--first-item ">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="first-item__img"> -->
            <div class="first-item__logo-title">goahead</div>
        </div>
        <div class="design-logo--first-item dark">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="first-item__img"> -->
            <div class="first-item__logo-title">goahead</div>
        </div>
        <div class="design-logo--second-item dark second-item__row mt-40">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="second-item__img"> -->
            <div class="second-item__logo-title second-item__logo-title-big"><span>go</span></div>
        </div>
        <div class="design-logo--second-item second-item__row mt-40">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="second-item__img"> -->
            <div class="second-item__logo-title second-item__logo-title-big">go</div>
        </div>
        
        <div class="design-logo--second-item dark second-item__row mt-40">
            <!-- <img src="@/assets/img/logos/main.svg" alt="logo" class="second-item__img"> -->
            <div class="second-item__logo-title second-item__logo-title-big">go</div>
        </div>
        <!-- <div class="design-logo--second-item second-item__row">
            <img src="@/assets/img/logos/main.svg" alt="logo" class="second-item__img">
        </div>
        <div class="design-logo--second-item dark second-item__row">
            <img src="@/assets/img/logos/white.svg" alt="logo" class="second-item__img">
        </div>
        <div class="design-logo--second-item ">
            <img src="@/assets/img/logos/black.svg" alt="logo" class="second-item__img">
        </div> -->
    </div>
    <h3 class="text-prime mb-40"><b>Правила использования</b></h3>
    <div class="design-logo-rules">
        <div class="design-logo-rule">
            <span class="rule-num">1</span>
            <p class="rule-text text-second">Логотип должен легко считываться</p>
        </div>
        <div class="design-logo-rule">
            <span class="rule-num">2</span>
            <p class="rule-text text-second">Фон должен быть однородным, не пестрым</p>
        </div>
        <div class="design-logo-rule">
            <span class="rule-num">3</span>
            <p class="rule-text text-second">Если оранжевый цвет конфликтует с фоном, ставить монохромный вариант</p>
        </div>
    </div>
    <div class="design-logo-cards">
        <div class="design-logo-card">
            <div class="design-logo-card__img">
                <img src="@/assets/img/rule/1.jpg" class="" alt="card__img">
            </div>
            <p class="design-logo-card__text">Изменение цвета</p>
        </div>
        <div class="design-logo-card">
            <div class="design-logo-card__img">
                <img src="@/assets/img/rule/2.jpg" class="" alt="card__img">
            </div>
            <p class="design-logo-card__text">Использование на ярких цветах</p>
        </div>
        <div class="design-logo-card">
            <div class="design-logo-card__img">
                <img src="@/assets/img/rule/3.jpg" class="" alt="card__img">
            </div>
            <p class="design-logo-card__text">Использование на насыщенной фотографии</p>
        </div>
        <div class="design-logo-card">
            <div class="design-logo-card__img">
                <img src="@/assets/img/rule/4.jpg" class="" alt="card__img">
            </div>
            <p class="design-logo-card__text">Несоблюдение пропорций
                и трансформация</p>
        </div>
    </div>
    <div class="design-logo-buttons">
        <a href="https://disk.yandex.ru/d/TxA_T6o5lwQ07Q" target="_blank" class="btn design-logo-buttons-item ">Логотипы на Яндекс.Диске</a>
        <a href="https://www.figma.com/file/q6vM5yHOzyf4BMqnvw8Da7/Go-Ahead-bb?node-id=347-659&t=tqAgZ2EkPhy9pZ7B-0" class="btn btn-light  " target="_blank">Логотипы в фигме</a>
    </div>
</template>
<style lang="scss">
@use "@/assets/scss/abstracts" as *;

.design-logo-wrapper {
    max-width: 716px;
    margin-bottom: 120px;
}

.design-logo--first-list,
.design-logo--second-list {
    margin-top: 40px;
    margin-bottom: 120px;
    @include flex(row, center, stretch);
    flex-wrap: wrap;
}
.design-logo--second-list {
    margin-bottom: 220px;
}
.design-logo--first-item,
.design-logo--second-item {
    max-width: 514px;
    width: 100%;
    padding: 51px 0;
    min-height: 195px;
    background: $white;
    border: 1px solid $black;
    @include flex(column, center, center);
    text-align: center;

    &.dark {
        background: $light-black;
        color: $white;
    }
}
// .design-logo--first-item{
//     margin-bottom: ;
// }
.first-item,
.second-item {
    &__img {
        max-width: 150px;
        width: 100%;
    }

    &__logo-title {
        font-size: 49.1403px;
        line-height: 60px;
        font-weight: 700;
        margin: 5px;

        span {
            color: $orange;
        }
    }
}

.design-logo--second-item {
    max-width: 343.33px;
    padding: 47px 0;
}

.second-item {
    &__row {
        @include flex(row, center, center);
    }

    &__img {
        max-width: 90px;
    }

    &__logo-title {
        font-size: 28.9982px;
        line-height: 35px;
        &-big{
        line-height: 75px;
            font-size: 70px;
        }
    }
}

.design-logo {
    
    &-rules {
        @include flex(row, space-between, center);
    }

    &-rule {
        @include flex(row, space-between, center);
        max-width: 417px;
        width: 100%;

        .rule-num {
            font-family: 'Robtronika';
            font-weight: 400;
            font-size: 52px;
            line-height: 60px;
            margin-right: 15px;
        }
    }

    &-cards {
        @include flex(row, center);
        gap: 16px;
        margin-top: 82px;
    }

    &-card {
        max-width: 216px;
        width: 100%;

    }

    &-card__img {
        width: 100%;
        position: relative;

        img {
            width: 100%;
        }

        &::after {
            content: '';
            position: absolute;
            width: 140%;
            height: 3px;
            background: $red;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) rotate(42deg);
        }
    }

    &-card__text {
        font-size: 15px;
        line-height: 20px;
        margin-top: 23px;
    }

    &-buttons {
        margin-top: 140px;
        @include flex(row, center, center);
        gap: 150px;
        &-item{
        max-width: 475px
    }
    }

  
}
</style>
