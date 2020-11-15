<template>

        <v-container>
            <v-row>

                <v-col
                        class="d-flex flex-row-reverse">
                    <v-sheet
                            rounded="lg"
                            class="px-4 pt-4 pb-3"
                            height="500"
                            width="500"
                            elevation="6"
                    >
                        <v-container >
                            <v-row>
                                <v-col>
                                    <p class="text-sm-left" style="color: rgba(0,0,0,0.6);font-weight: bold ;font-size: 30px">院校专业查询</p>
                                </v-col>
                                <v-col>
                                    <p class="text-sm-right" style="color: rgba(0,0,0,0.6);font-weight: bold ;font-size: 20px ">辽宁</p>
                                </v-col>
                            </v-row>

                            <v-row>
                                <v-col >
                                    <p class="text-sm-left" style="color: rgba(0,0,0,0.6);;font-weight: bold;font-size: 30px ">总分</p>
                                </v-col>
                            </v-row>
                            <br>
                            <v-row>
                                <v-text-field
                                        label="分数 "
                                        placeholder="0~750"
                                        outlined
                                        suffix="分"
                                ></v-text-field>
                            </v-row>
                            <br>
                            <v-row >
                                <v-btn  class="pa-md-4 mx-lg-auto" color="primary" elevation="4" x-large width="250px" style="font-size: 20px;">
                                    一键分析
                                </v-btn>
                            </v-row>
                        </v-container>

                    </v-sheet>
                </v-col>
            </v-row>
        </v-container>

</template>

<script>
    export default {
        name: "page"
    }
</script>

<style scoped>

</style>