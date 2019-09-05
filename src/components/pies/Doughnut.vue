<template>
    <chart
            :options="option"
            :auto-resize="true"
            style="width: 100%; height: 100%;"
    />
</template>

<script type="text/ecmascript-6">
    export default {
        name: "Doughnut",
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
                legend: {
                    orient: 'vertical',
                    x: 'left',
                    data:['直接访问','邮件营销','联盟广告','视频广告','搜索引擎'],
                    textStyle:{
                        color:'white'
                    }
                },
                series: [
                    {
                        name:'访问来源',
                        type:'pie',
                        radius: ['50%', '70%'],
                        avoidLabelOverlap: false,
                        label: {
                            normal: {
                                show: false,
                                position: 'center'
                            },
                            emphasis: {
                                show: true,
                                textStyle: {
                                    fontSize: '30',
                                    fontWeight: 'bold'
                                }
                            }
                        },
                        labelLine: {
                            normal: {
                                show: false
                            }
                        },
                        data:[
                            {value:335, name:'直接访问'},
                            {value:310, name:'邮件营销'},
                            {value:234, name:'联盟广告'},
                            {value:135, name:'视频广告'},
                            {value:1548, name:'搜索引擎'}
                        ]
                    }
                ]
            };

        }
    };
</script>

<style lang="stylus" rel="stylesheet/stylus">

</style>
