<template>
    <OverlayScrollbars class="list"
                       :options="{ className: 'os-theme-light', scrollbars: { autoHide: 'l', autoHideDelay: 100 } }">
        <div class="list-item" v-for="item in 50" :key="item">{{item}}</div>
    </OverlayScrollbars>
</template>

<script>
  import 'overlayscrollbars/css/OverlayScrollbars.css'
  import {OverlayScrollbarsComponent} from 'overlayscrollbars-vue'

  export default {
    name: 'Playground',
    components: {OverlayScrollbars: OverlayScrollbarsComponent},
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .list {
        height: 100vh;
        width: 64px;
        background-color: #434d68;
    }

    .list-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        height: 70px;
        color: #999999;
        cursor: pointer;
    }

    .list-item:hover {
        background-color: #586078;
        color: #fff;
    }
</style>
