<template>
  <form>
    <h2>口味 ❤️</h2>
    <template v-for="style in ramenStyle" :key="style">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="radio"
                name="ramenStyle" :id="style"
            />
            <label class="form-check-label" :for="style">
                {{ style }}
            </label>
        </div>
    </template>

    <h2>湯底醬汁</h2>
    <template v-for="sauce in sauces" :key="sauce">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="radio"
                name="sauces" :id="'sauce_' + sauce"
            />
            <label class="form-check-label" :for="'sauce_' + sauce">
                {{ sauce }}
            </label>
        </div>
    </template>

    <h2>風味油</h2>
    <template v-for="oil in oils" :key="oil">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="radio"
                name="oils" :id="'oil_' + oil"
            />
            <label class="form-check-label" :for="'oil_' + oil">
                {{ oil }}
            </label>
        </div>
    </template>

    <h2>叉燒 🥩</h2>
    <template v-for="meat in meats" :key="meat">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="radio"
                name="meats" :id="'meat_' + meat"
            />
            <label class="form-check-label" :for="'meat_' + meat">
                {{ meat }}
            </label>
        </div>
    </template>

    <h2>麵體 🍜</h2>
    <template v-for="noodle in noodles" :key="noodle">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="radio"
                name="noodles" :id="'noodle_' + noodle"
            />
            <label class="form-check-label" :for="'noodle_' + noodle">
                {{ noodle }}
            </label>
        </div>
    </template>

    <h2>蔬菜 🌽</h2>
    <template v-for="veg in vegetables" :key="veg">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="checkbox"
                name="vegetables" :id="'veg_' + veg"
            />
            <label class="form-check-label" :for="'veg_' + veg">
                {{ veg }}
            </label>
        </div>
    </template>

    <h2>辛味 🌶️</h2>
    <div>
        <label for="customRange3" class="form-label">{{ spicy }} 辛 {{ howSpicy }}</label>
        <input type="range" class="form-range" v-model="spicy"
        min="0" max="5" step="1" id="customRange3">
    </div>

    <h2>飲料 🍺</h2>
    <template v-for="drink in drinks" :key="drink">
        <div class="form-check d-inline-block mx-3">
            <input class="form-check-input" type="radio"
                name="drinks" :id="'drink_' + drink"
            />
            <label class="form-check-label" :for="'drink_' + drink">
                {{ drink }}
            </label>
        </div>
    </template>


  </form>
</template>

<script>
export default {
    data() {
        return {
            ramenStyle : ['醬油', '味噌', '鹽味', '豚骨'],
            sauces: ['淡', '普通', '濃'],
            oils: ['無', '淡', '普通', '濃', '超濃'],
            meats: ['無', '圓叉燒', '方叉燒'],
            vegetables: ['青蔥', '高麗菜', '玉米粒', '海苔', '黑木耳'],
            noodles: ['軟', '普通', '硬'],
            additionals: ['半熟蛋', '雙倍叉燒'],
            spicy: 0,
            drinks: ['水', '可樂', '可爾必思', '啤酒']

        }
    },

    computed: {
        howSpicy: function(){
            return this.spicy >=3 ? "這真的很辣" : ""
        }
    }


};
</script>

<style>
h2 {
    display: block;
    border-bottom: orange 1px solid;
    padding-bottom: 2px;
    font-size: 1.5rem !important;
    margin-top: 1rem !important;
}

</style>