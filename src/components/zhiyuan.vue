<template>
    <v-container>
        <v-tabs v-model="tabs">
            <v-tab href="#tabaa">院校优先</v-tab>
            <v-tab href="#tab2">专业优先</v-tab>
        </v-tabs>
        <v-tabs-items v-model="tabs">
            <v-tab-item :value="'tabaa'">
                <v-expansion-panels>
                    <v-expansion-panel>
                        <v-expansion-panel-header >
                          筛选
                        </v-expansion-panel-header>
                        <v-expansion-panel-content>
                           <v-container>
                             <el-checkbox-group  v-model="checkedCities">
                               <el-checkbox v-for="city in cities" :label="city" :key="city">{{city}}</el-checkbox>
                             </el-checkbox-group>
                           </v-container>
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-tab-item>
        </v-tabs-items>

    </v-container>

</template>

<script>
const cityOptions = ['上海', '北京', '广州', '深圳'];
    export default {
        name: "zhiyuan",
        data () {
            return {
              checkedCities: [],
              cities: cityOptions,
                tabs: null,
                // text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
            }
        },
    }
</script>

<style scoped>

</style>