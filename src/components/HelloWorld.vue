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
                   @click="$router.push(link.url)"

            >
              {{link.title}}
            </v-btn>
          </template>

          <v-list
          >
            <v-list-item
                    v-for="subitem in link.data"
                    :key="subitem.title"
            >
              <v-list-item-title>{{subitem.title}}</v-list-item-title>
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
    <v-main class="grey lighten-3">
    <router-view></router-view>
      </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      links: [{title:'主页',
        url:'/page',
        data:[
          { title: 'Csdfack Me' },
          { title: 'Casdf Me' },
          { title: 'Clidf asdf2' },
        ]},
        {title:'志愿推荐',url:'/page',
          data:[
            { title: 'Csdqw234353Me' },
            { title: 'Casd2342134e' },
          ]},
        {title:'查询',url:'/page',
          data:[
            { title: '上当了发哈沙雕番Me' },
            { title: 'C阿瑟地方34e' },
          ]},
        {title:'智能配置',url:'/page',
          data:[
            { title: '上当了发哈沙雕番Me' },
            { title: 'C阿瑟地方34e' },
            { title: 'C阿瑟地方34e' },
            { title: 'C阿瑟地方34e' },
            { title: 'C阿瑟地方34e' },
          ]},
      ],
    }),
  }
</script>