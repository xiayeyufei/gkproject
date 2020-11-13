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

                <v-menu
                        class="d-flex justify-start mb-6 "
                        offset-y
                        open-on-hover
                        v-for="link in links"
                        :key="link"

                >
                    <template v-slot:activator="{ on, attrs }" >
                        <v-btn class="white"
                                elevation=0
                                v-bind="attrs"
                                v-on="on"

                        >
                            {{link.title}}
                        </v-btn>
                    </template>

                    <v-list>
                        <v-list-item
                                v-for="(item, index) in items"
                                :key="index"
                        >
                            <v-list-item-title>{{ item }}</v-list-item-title>
                        </v-list-item>
                    </v-list>
                    <v-spacer></v-spacer>
                </v-menu>

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
            items:[ [{ title: 'Click Me' },],
                [{ title: 'Click Me' },
                { title: 'Click Me' },
                { title: 'Click Me 2' }],
                [{ title: 'Cl Me' },
                { title: 'Cl Me' },
                { title: 'Clie 2' }],
                { title: 'Csdfack Me' },
                { title: 'Casdf Me' },
                { title: 'Clidf asdf2' },]
        }),
    }
</script>

<style scoped>

</style>