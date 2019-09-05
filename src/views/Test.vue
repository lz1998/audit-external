<template>
    <div class="test">
        <el-row style="height:300px;">
            <el-col :span="6" style="height:100%;">
                <SimpleBar></SimpleBar>
            </el-col>
            <el-col :span="6" style="height:100%;">
                <Doughnut></Doughnut>
            </el-col>
        </el-row>
        <el-row style="height:500px;">
            <el-col :offset="6" :span="12" style="height:100%;">
                <Map></Map>
            </el-col>
        </el-row>
    </div>
</template>

<script type="text/ecmascript-6">
    import Doughnut from '@/components/pies/Doughnut'
    import SimpleBar from '@/components/bars/SimpleBar'
    import Map from '@/components/maps/Map'
    export default {
        name: "Test",
        components:{
            Doughnut,
            SimpleBar,
            Map
        }
    };
</script>

<style>
    div{
        background-color: #0C164E;
    }
</style>
