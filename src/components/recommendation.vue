<template>
    <v-main class="grey lighten-3">
        <v-container>
            <v-row>
                <v-col cols="2">
                    <v-sheet rounded="lg">
                        <v-list color="transparent">
                            <v-list-item
                                    v-for="n in 5"
                                    :key="n"
                                    link
                            >
                                <v-list-item-content>
                                    <v-list-item-title>
                                        List Item {{ n }}
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-list-item>

                            <v-divider class="my-2"></v-divider>

                            <v-list-item
                                    link
                                    color="grey lighten-4"
                            >
                                <v-list-item-content>
                                    <v-list-item-title>
                                        Refresh
                                    </v-list-item-title>
                                </v-list-item-content>
                            </v-list-item>
                        </v-list>
                    </v-sheet>
                </v-col>

                <v-col
                        class="d-flex flex-row-reverse">
                    <v-sheet
                            rounded="lg"
                            class="d-flex mt-auto"

                            height="500"
                            width="500"
                    >

                    </v-sheet>
                </v-col>
            </v-row>
        </v-container>
    </v-main>
</template>

<script>
    export default {
        name: "recommendation"
    }
</script>

<style scoped>

</style>