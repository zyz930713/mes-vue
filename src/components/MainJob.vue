<template>
    <div>
        <el-form ref="searchForm" :model="searchForm" :rules="rules" label-width="120px">
            <el-row>
                <el-col :span="6">
                    <el-form-item label="工单号" prop="name">
                        <el-input v-model="searchForm.name" placeholder="请输入工单号"></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="6">
                    <el-form-item label="型号" prop="name">
                        <el-input v-model="searchForm.name" placeholder="请输入型号"></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="6">
                    <el-form-item label="线别" prop="name">
                        <el-input v-model="searchForm.name" placeholder="请输入线别"></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="6">
                    <el-form-item label="入库时间" prop="name">
                        <el-date-picker v-model="dateValue" type="datetime" placeholder="请输入起始时间"></el-date-picker>
                        <el-date-picker v-model="dateValue" type="datetime" placeholder="请输入结束时间"></el-date-picker>
                    </el-form-item>
                </el-col>
            </el-row>
            <el-row>
                <el-col :span="6">
                    <el-form-item label="计划人" prop="name">
                        <el-input v-model="searchForm.name" placeholder="请输入计划人"></el-input>
                    </el-form-item>
                </el-col>
                <el-col :span="6">
                    <el-form-item label="进度" prop="name">
                        <el-select v-model="searchForm.region" placeholder="请选择进度">
                            <el-option label="入库完成" value="1"></el-option>
                            <el-option label="进行中" value="0"></el-option>
                        </el-select>
                    </el-form-item>
                </el-col>
                <el-col :span="6">
                    <el-form-item label="关闭时间" prop="name">
                        
                        <el-date-picker v-model="dateValue" type="datetime" placeholder="请输入起始时间"></el-date-picker>
                        <el-date-picker v-model="dateValue" type="datetime" placeholder="请输入结束时间"></el-date-picker>
                    </el-form-item>
                </el-col>
                <el-col :span="6">
                    <el-form-item>
                        <el-button type="primary" @click="submit('loginForm')">点击查询</el-button>
                    </el-form-item>
                </el-col>
            </el-row>
                <!-- <el-button type="primary" @click="submit('loginForm')">登陆</el-button>
                <el-button @click="resetForm('loginForm')">重置</el-button> -->
        </el-form>
        <el-table :data= "tableData" border :stripe="true" style="width: 100%; margin-top:20px">
            <el-table-column label="序列" width="50" prop="xulie"></el-table-column>
            <el-table-column label="工单号" width="110" prop="jobNumber"></el-table-column>
            <el-table-column label="型号" width="110" prop="xinghao"></el-table-column>
            <el-table-column label="线别" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="入库进度" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="入库" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="计划人" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="计划数量" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="产线合格品" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="产线损失" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="最终合格品" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="最终良率" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="实收合格品" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="最终报废" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="剩余" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="投产时间" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="最后时间" width="110" prop="xianbie"></el-table-column>
            <el-table-column label="周转时间" width="110" prop="xianbie"></el-table-column>
        </el-table> 
    </div>
</template>


<script>
export default {
    data(){
        return {
            searchForm: {
                name: "",
                region: ""
            },
            tableData: [
                {
                    xulie: 1,
                    jobNumber: 123,
                    xinghao: "acs123",
                    xianbie: "A1"
                },
                {
                    xulie: 1,
                    jobNumber: 123,
                    xinghao: "acs123",
                    xianbie: "A1"
                },
                {
                    xulie: 1,
                    jobNumber: 123,
                    xinghao: "acs123",
                    xianbie: "A1"
                }
            ],
            dateValue: "",
            rules: {
                name:{
                    required: true,
                    message: "111",
                    trigger: "blur"
        }
    }
        }
    }
    
}
</script>
