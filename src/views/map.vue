<script setup>
    const defaultProps = {
        children: 'children',
        label: 'label',
    }
    const data = [
        {
            id: 1,
            label: '公共设施',
            children: [
                {
                    id: 1-1,
                    label: '各类井盖',
                },
                {
                    id: 1-2,
                    label: '监控电子眼',
                },
                {
                    id: 1-3,
                    label: '立杆',
                },
                {
                    id: 1-4,
                    label: '路灯',
                },
                {
                    id: 1-5,
                    label: '消防设施',
                },
                {
                    id: 1-6,
                    label: '信息亭',
                },
                {
                    id: 1-7,
                    label: '邮筒',
                },
                {
                    id: 1-8,
                    label: '雨水箅子',
                },
                {
                    id: 1-9,
                    label: '邮筒',
                },
                {
                    id: 1-10,
                    label: '治安岗亭',
                },
            ],
        },
        {
            id: 2,
            label: '道路交通',
            children:[
                {
                    id:2-1,
                    label:'路名牌'
                },
                {
                    id:2-2,
                    label:'交通标志牌'
                },
                {
                    id:2-3,
                    label:'跨河桥'
                },
                {
                    id:2-4,
                    label:'公交站亭'
                },
                {
                    id:2-5,
                    label:'停车场'
                },
            ]
        },
        {
            id: 3,
            label: '房屋土地',
            children:
            [
                {
                    id:3-1,
                    label:'宣传栏'
                }
            ]

        },
        {
            id: 4,
            label: '市容环境',
            children:
            [
                {
                    id:4-1,
                    label:'垃圾箱'
                },
                {
                    id:4-2,
                    label:'化粪池'
                }
            ]

        },
        {
            id: 5,
            label: '园林绿化',
            children:
            [
                {
                    id:5-1,
                    label:'街头座椅'
                },
                {
                    id:5-2,
                    label:'喷泉'
                },
                {
                    id:5-2,
                    label:'雕塑'
                }
            ]

        },
        {
            id: 6,
            label: '其他设施',
            children:
            [
                {
                    id:6-1,
                    label:'防汛墙'
                }
              
            ]

        }

    ]

</script>

<template>
    <div class="map-page">
        <el-header>
            <div class="header-left">
                <img id="logo" src="../assets/img/xiaohui2.png" />
                <p>校园地图信息管理平台</p>
            </div>
            <div class="header-right">
                <el-button type="primary">
                    <router-link to="/" class="header-link">返回首页</router-link>
                </el-button>
            </div>
        </el-header>


        <div class="map-container">
            <BMap :tilt="0" :height="850" :center="{ lng: 117.1502, lat: 34.2200 }" :zoom="16" :minZoom="3"
                enableScrollWheelZoom enableDragging />
        </div>

        <div class="map-on">
            <el-card style="width: 400px" shadow="always">
                <p>校园部件展示</p>
                <el-tree style="max-width: 600px" :data="data" show-checkbox node-key="id" :props="defaultProps" />
            </el-card>
        </div>

    </div>
</template>



<style scoped src="../assets/map.css">

</style>