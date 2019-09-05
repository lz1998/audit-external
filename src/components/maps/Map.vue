<template>
    <el-amap vid="amapDemo">
    </el-amap>
</template>

<script type="text/ecmascript-6">
    export default {
        name: "Map",
        data(){
            return{
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
