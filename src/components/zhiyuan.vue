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
                            Item
                            <template v-slot:actions>
                                <v-icon color="primary" left>

                                </v-icon>
                            </template>
                        </v-expansion-panel-header>
                        <v-expansion-panel-content>
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-tab-item>
        </v-tabs-items>

    </v-container>

</template>

<script>
    export default {
        name: "zhiyuan",
        data () {
            return {
                tabs: null,
                // text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
            }
        },
    }
</script>

<style scoped>

</style>