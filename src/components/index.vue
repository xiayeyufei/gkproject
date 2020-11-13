<template>
    <v-app id="inspire">
        <v-app-bar
                app
                color="white"
                flat
        >
            <v-container class="py-0 fill-height">
                <v-avatar
                        class="mr-10"
                        color="grey darken-1"
                        size="32"
                ></v-avatar>

                <v-btn
                        v-for="link in links"
                        :key="link.title"
                        @click="link.url"
                        text
                >
                    {{ link .title}}
                </v-btn>

                <v-spacer></v-spacer>

                <v-responsive max-width="260">
                    <v-text-field
                            dense
                            flat
                            hide-details
                            rounded
                            solo-inverted
                    ></v-text-field>
                </v-responsive>
            </v-container>
        </v-app-bar>
        <router-view></router-view>
    </v-app>
</template>

<script>
    export default {
        name: "index",
        data: () => ({
            links: [{title:'主页',url:'/page'},
                {title:'志愿推荐',url:'/page'},
                {title:'查询',url:'/page'},
                {title:'智能配置',url:'/page'},

            ],
        }),
    }
</script>

<style scoped>

</style>