<template>
    <div class="home">
        <div id="map"></div>
    </div>
</template>

<script>
import echarts from "echarts";
import mapData from "@/geo";

export default {
    name: "Home",
    data() {
        return {
            myChart: null,
        };
    },
    methods: {
        initMap() {
            this.myChart = echarts.init(document.getElementById("map"));
            echarts.registerMap("world", mapData); // 定义名称下面要用, 这样做的好处就是可以很方便的实现切换地图的效果
            this.myChart.setOption({
                series: [
                    {
                        type: "map",
                        mapType: "world", // 自定义扩展图表类型
                        label: {
                          show: false,
                        },
                    },
                ],
            });
        },
    },
    mounted() {
        this.initMap();
    }
}
</script>

<style scoped>
    .home {
        height: 100vh;
    }
</style>