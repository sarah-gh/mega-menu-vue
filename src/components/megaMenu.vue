<template>
    <div class="container-Menu">
        <a class="name" @click="menu" >
          {{ title }}
        </a>
        <div v-show="show" v-click-outside="hide" class="mega-menu">
            <p @click="hide" class="mega-menu_close">
                <img src="@/assets/close.svg" />
            </p>
            <div>
                <div v-for="(item, i) in list" :key="'x-'+i" class="mega-menu_categories">
                    <h3 @mouseover="showItems(i)" :class="[index !== i ? '' : 'active']" @click="showCategory(item)">
                        {{ item.title }}
                    </h3>
                </div>
            </div>
            <div>
                <div v-for="(item, i) in list" :key="'y-'+i" class="mega-menu_items">
                    <div v-if="index == i">
                        <p v-for="(data, j) in item[array]" :key="'z-'+j" @click="showItem(data)">
                            {{ data.title }}
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
  name: 'megaMenu',
  props: {
    list: {
      type: Array
    },
    array: {
      type: String
    },
    title: {
      type: String
    }
  },
  data () {
    return {
      show: false,
      index: 0
    }
  },
  methods: {
    menu () {
      setTimeout(() => {
        this.show = !this.show
      }, 0)
    },
    hide () {
      this.show = false
    },
    showItem (data) {
      this.$emit('showItem', data)
    },
    showCategory (data) {
      this.$emit('showCategory', data)
    },
    showItems (i) {
      this.index = i
    }
  }
}
</script>

<style lang="scss" scoped>
.container-Menu {
    direction: rtl;
    width: fit-content;
    .name {
        cursor: pointer;
    }
}
.mega-menu {
    position: absolute;
    top: 60px;
    left: 50%;
    width: 80%;
    transform: translate(-50%, 0%);
    max-width: 800px;
    background-color: white;
    border-radius: 20px;
    box-shadow: 0px 2px 3px black;
    padding: 25px 50px 15px 15px;
    display: flex;
    gap: 10px;
    &_close {
        position: absolute;
        right: 15px;
        top: 15px;
        margin: 0;
        padding: 0;
    }
    &_categories {
        width: 200px;
        h3 {
            font-size: 20px;
            text-align: right;
            padding: 4px 10px;
            margin: 0;
            margin-bottom: 12px;
            cursor: pointer;
        }
        .active {
            background-color: #8c7191;
            color: white;
            border-radius: 4px;
        }
    }
    &_items {
        > div{
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            p {
                cursor: pointer;
            }
        }
    }
}
</style>
