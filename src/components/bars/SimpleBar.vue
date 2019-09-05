<template>
    <chart
            :options="option"
            :auto-resize="true"
            style="width: 100%; height: 100%;"
    />
</template>

<script type="text/ecmascript-6">
    export default {
        name: "SimpleBar",
        props:{
            data: {
                type: Array,
                default: () => {
                    return [
                        ['啊啊 啊', '2012'],
                        ['浙江', 1500],
                        ['上海', 1200],
                        ['江苏',600],
                        ['广东',250],
                        ['北京',300],
                        ['深圳',300],
                        ['安徽',900]
                    ]
                }
            },
            itemColor:{
                type: String,
                default: () => {
                    return '#27D08A'
                }
            }
        },
        data() {
            return {
                option: {}
            }
        },
        mounted() {
            let _this=this;
            this.option = {
                dataset:{
                    source:_this.data
                },
                xAxis: {
                    type: 'category',
                    axisLabel:{
                        color:'white'
                    },
                    axisLine:{
                        lineStyle:{
                            color:'white'
                        }
                    }
                },
                yAxis: {
                    type: 'value',
                    axisLabel:{
                        color:'white'
                    },
                    axisLine:{
                        lineStyle:{
                            color:'white'
                        }
                    }
                },
                series: [
                    {
                        type: 'bar',
                        itemStyle:{
                            barBorderRadius:5,
                            color:_this.itemColor
                        }
                    }
                ]
            };

        }
    };
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
