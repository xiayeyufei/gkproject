<template>
    <v-container>
      <v-row>
        <v-col>
          <v-tabs v-model="tabs">
            <v-tab href="#tabaa">院校优先</v-tab>
            <v-tab href="#tab2">专业优先</v-tab>
          </v-tabs>
        </v-col>
        <v-col>
          <v-row class="demo-input-suffix">
            <div class="demo-input-suffix">
              <el-input v-model="input" placeholder="意向院校" label="属性方式："><i slot="prefix" class="el-input__icon el-icon-search"></i></el-input>
            </div>
            <v-btn  class="mb-6" color="light-blue lighten-1" elevation="3"  width="50px" style="font-size: 15px;color:white">
              搜索
            </v-btn>
          </v-row>
        </v-col>

      </v-row>

        <v-tabs-items v-model="tabs">
            <v-tab-item :value="'tabaa'">
                <v-expansion-panels>
                    <v-expansion-panel>
                      <v-expansion-panel-header v-slot="{ open }">
                        <v-row no-gutters>
                          <v-col cols="4">

                          </v-col>
                          <v-col cols="4">

                          </v-col>
                          <v-col
                              cols="8"
                              class="text--secondary"
                          >
                            <v-fade-transition leave-absolute>
                              <span v-if="open">收起</span>
                              <v-row
                                  v-else
                                  no-gutters
                                  style="width: 100%"
                              >
                                  筛选展开
                              </v-row>
                            </v-fade-transition>
                          </v-col>
                        </v-row>
                      </v-expansion-panel-header>

                        <v-expansion-panel-content>
                           <v-container style="text-align: left">
                             院校省份
                             <el-checkbox-group  v-model="checkedCities">
                               <el-checkbox v-for="city in cities" :label="city" :key="city">{{city}}</el-checkbox>
                             </el-checkbox-group>
                             <el-divider></el-divider>
                             院校类型
                             <el-checkbox-group  v-model="checkedType">
                               <el-checkbox v-for="Type in Types" :label="Type" :key="Type">{{Type}}</el-checkbox>
                             </el-checkbox-group>
                             <el-divider></el-divider>
                             热门标签
                             <el-checkbox-group  v-model="checkedLable">
                               <el-checkbox v-for="Lable in Lables" :label="Lable" :key="Lable">{{Lable}}</el-checkbox>
                             </el-checkbox-group>
                             <v-row >
                               <v-btn  class="pa-md-4 mx-lg-auto" color="light-blue lighten-1" elevation="4" large width="200px" style="font-size: 17px;color:white">
                                 一键筛选
                               </v-btn>
                             </v-row>
                           </v-container>
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-tab-item>
        </v-tabs-items>

    </v-container>

</template>

<script>
const cityOptions = ['辽宁','安徽','北京','重庆','福建','广东','广西','甘肃','贵州','河北','河南','海南','湖北','湖南','黑龙江','吉林','江苏','江西','内蒙古','宁夏','青海','上海','四川','山东','山西','陕西','天津','新疆','西藏','云南','浙江'];
const schoolType =['综合','理工','财经','农林','医药','师范','体育','政法','艺术','民族','军事','语言','其它']
const schoolLable =['办公','民办','中外/港澳台','985','211','双一流']
export default {
        name: "zhiyuan",
        data () {
            return {
              checkedCities: [],
              cities: cityOptions,
              checkedType: [],
              Types: schoolType,
              checkedLable:[],
              Lables:schoolLable,
                tabs: null,
                // text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
            }
        },
    }
</script>

<style scoped>

</style>