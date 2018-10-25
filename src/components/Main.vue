<template>
    <el-container>
            <el-aside>
                <el-col :span="20" :offset="2">
                    <el-menu default-active="2" :unique-opened="true" :router="true" class="el-menu-vertical-demo"
                        @open="handleOpen" @close="handleClose" background-color="#545c64" text-color="#fff"
                        active-text-color="#ffd04b">
                        <!-- 监控工单 -->
                        <el-submenu index="1">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>监控工单</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="/main/mainJob">主工单列表</el-menu-item>
                                <el-menu-item index="1-2">子工单列表</el-menu-item>
                                <el-menu-item index="1-3">预入库记录</el-menu-item>
                                <el-menu-item index="1-4">预报废记录</el-menu-item>
                                <el-menu-item index="1-5">材料查询</el-menu-item>
                                <el-menu-item index="1-6">job优先级</el-menu-item>
                                <el-menu-item index="1-7">HOLD工单</el-menu-item>
                                <el-menu-item index="1-8">RELESE工单</el-menu-item>
                                <el-menu-item index="1-9">工单HOLD报告</el-menu-item>
                                <el-menu-item index="1-10">二维码报表</el-menu-item>
                                <el-menu-item index="1-11">WII</el-menu-item>
                                <el-menu-item index="1-12">缺陷代码分布</el-menu-item>
                            </el-menu-item-group>
                            <el-menu-item-group title="分组2">
                                <el-menu-item index="1-2-1">选项3</el-menu-item>
                            </el-menu-item-group>
                            <el-submenu index="1-4">
                                <template slot="title">选项4</template>
                                <el-menu-item index="1-4-1">选项1</el-menu-item>
                            </el-submenu>
                        </el-submenu>
                        <!-- 仓库报告 -->
                        <el-submenu index="2">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>仓库报告</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="2-1">包装报表</el-menu-item>
                                <el-menu-item index="2-2">交货报表</el-menu-item>
                                <el-menu-item index="2-3">客退报告</el-menu-item>
                                <el-menu-item index="2-4">包装计划</el-menu-item>
                                <el-menu-item index="2-5">KIPC包装计划</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <!-- 定制报告 -->
                        <el-submenu index="3">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>定制报告</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="3-1">工单周转</el-menu-item>
                                <el-menu-item index="3-2">工单完成</el-menu-item>
                                <el-menu-item index="3-3">生产报告</el-menu-item>
                                <el-menu-item index="3-4">检查箱号</el-menu-item>
                                <el-menu-item index="3-5">生产追朔和控制</el-menu-item>
                                <el-menu-item index="3-6">Pot膜物料查询</el-menu-item>
                                <el-menu-item index="3-7">物料分配管理</el-menu-item>
                                <el-menu-item index="3-8">物料记录查询</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <el-submenu index="4">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>良率报告</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="4-1">一次良率报告</el-menu-item>
                                <el-menu-item index="4-2">最终良率报告</el-menu-item>
                                <el-menu-item index="4-3">原材料良率关系表</el-menu-item>
                                <el-menu-item index="4-4">工单良率</el-menu-item>
                                <el-menu-item index="4-4">OQC PPM报告</el-menu-item>
                                <el-menu-item index="4-6">Station日良率</el-menu-item>
                                <el-menu-item index="4-7">操作员周产出报告</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <el-submenu index="5">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>系统设置</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="5-1">工厂</el-menu-item>
                                <el-menu-item index="5-2">生产区段</el-menu-item>
                                <el-menu-item index="5-3"> 家族</el-menu-item>
                                <el-menu-item index="5-4">系列</el-menu-item>
                                <el-menu-item index="5-4">子系列</el-menu-item>
                                <el-menu-item index="5-6">型号</el-menu-item>
                                <el-menu-item index="5-7">客户标签配置</el-menu-item>
                                <el-menu-item index="5-8"> 胶水&铜线工位配置</el-menu-item>
                                <el-menu-item index="5-9"> Check ABC</el-menu-item>
                                <el-menu-item index="5-10">包装配置</el-menu-item>
                                <el-menu-item index="5-11"> 生产目标设置</el-menu-item>
                                <el-menu-item index="5-12">制程</el-menu-item>
                                <el-menu-item index="5-13">站点</el-menu-item>
                                <el-menu-item index="5-14">步骤</el-menu-item>
                                <el-menu-item index="5-15">缺陷代码</el-menu-item>
                                <el-menu-item index="5-16">一般设置</el-menu-item>
                                <el-menu-item index="5-17"> 机器</el-menu-item>
                                <el-menu-item index="5-18">组</el-menu-item>
                                <el-menu-item index="5-19">Hold群组</el-menu-item>
                                <el-menu-item index="5-20">权限</el-menu-item>
                                <el-menu-item index="5-21">Tray关系</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <el-submenu index="6">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>系统管理</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="6-1">工程师</el-menu-item>
                                <el-menu-item index="6-2">角色</el-menu-item>
                                <el-menu-item index="6-3">客户端注册</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <el-submenu index="7">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>良率报告</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="7-1">一次良率报告</el-menu-item>
                                <el-menu-item index="7-2">最终良率报告</el-menu-item>
                                <el-menu-item index="7-3">原材料良率关系表</el-menu-item>
                                <el-menu-item index="7-4">工单良率</el-menu-item>
                                <el-menu-item index="7-4">OQC PPM报告</el-menu-item>
                                <el-menu-item index="7-6">Station日良率</el-menu-item>
                                <el-menu-item index="7-7">操作员周产出报告</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <el-submenu index="8">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>系统管理</span>
                            </template>
                            <el-menu-item-group>
                                <template slot="title">分组一</template>
                                <el-menu-item index="8-1">工程师</el-menu-item>
                                <el-menu-item index="8-2">角色</el-menu-item>
                                <el-menu-item index="8-3">客户端注册</el-menu-item>
                            </el-menu-item-group>
                        </el-submenu>
                        <el-submenu index="9">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>English</span>
                            </template>
                        </el-submenu>
                        <el-submenu index="10">
                            <template slot="title">
                                <i class="el-icon-location"></i>
                                <span>注销</span>
                            </template>
                        </el-submenu>
                    </el-menu>
                </el-col>
            </el-aside>
            <el-container>
                <el-header>
                    <el-col :span="24">
                        <el-menu :default-active="activeIndex2" :router="true" class="el-menu-demo" mode="horizontal"
                            @select="handleSelect" background-color="#545c64" text-color="#fff" active-text-color="#ffd04b">
                            <el-menu-item index="1">处理中心</el-menu-item>
                            <el-submenu index="2">
                                <template slot="title">我的工作台</template>
                                <el-menu-item index="/foo">选项1</el-menu-item>
                                <el-menu-item index="/bar">选项2</el-menu-item>
                                <el-menu-item index="2-3">选项3</el-menu-item>
                                <el-submenu index="2-4">
                                    <template slot="title">选项4</template>
                                    <el-menu-item index="2-4-1">选项1</el-menu-item>
                                    <el-menu-item index="2-4-2">选项2</el-menu-item>
                                    <el-menu-item index="2-4-3">选项3</el-menu-item>
                                </el-submenu>
                            </el-submenu>
                            <el-menu-item index="3" disabled>消息中心</el-menu-item>
                        </el-menu>
                    </el-col>


                </el-header>
                <el-main>
                    <router-view></router-view>
                </el-main>
            </el-container>
        </el-container>
</template>

<script>
export default {
  name: "Main",
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1"
    };
  },
  methods: {
            handleSelect(key, keyPath) {
                console.log(key, keyPath);
            },
            handleOpen(key, keyPath) {
                console.log(key, keyPath);
            },
            handleClose(key, keyPath) {
                console.log(key, keyPath);
            }
        }
};
</script>
