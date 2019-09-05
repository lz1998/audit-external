<template>
    <el-amap vid="amapDemo" :amap-manager="amapManager" :events="mapEvents"  class="amap-demo">
    </el-amap>
</template>

<script type="text/ecmascript-6">

    import VueAMap from 'vue-amap'
    let amapManager = new VueAMap.AMapManager();


    export default {
        name: "Map",
        data(){
            return{
                map:{},
                amapManager,
                mapEvents: {
                    init(o) {
                        o.setMapStyle('amap://styles/7299cf06a60ceba1c84cf3941afbdbe5');

                    }
                },
                layer:{},
                map:{}
            }
        },
        mounted() {

        }
    };
</script>

<style>
    .map{
        height: 100%;
        width: 100%;
        background-color: white;
    }

</style>
