<template>
  <v-app id="inspire">
    <v-app-bar
            app
            color="light-blue lighten-2"
            flat

    >
      <v-container class="py-0 fill-height">
        <v-avatar
                class="mr-10"
                color="grey darken-1"
                size="32"
        ></v-avatar>
        <v-btn class="light-blue lighten-2" style="color: white"
               elevation=0
               v-bind="attrs"
               v-on="on"
               @click="$router.push(link.url)"
        >
          主页
        </v-btn>
        <v-menu
                class="d-flex justify-start mb-6 "
                offset-y
                open-on-hover
                v-for="link in links"
                :key="link"

        >
          <template v-slot:activator="{ on, attrs }" >
            <v-btn class="light-blue lighten-2" style="color: white"
                   elevation=0
                   v-bind="attrs"
                   v-on="on"
                   @click="$router.push(link.url)"
            >
              {{link.title}}
              <i class="el-icon-caret-bottom"></i>
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
      links: [
        {title:'志愿推荐',url:'/page',
          data:[
            { title: '院校优先' },
            { title: '专业优先' },
          ]},
        {title:'查询',url:'/page',
          data:[
            { title: '查学校' },
            { title: '查专业' },
          ]},
        {title:'智能配置',url:'/page',
          data:[
            { title: '个性化筛选' },
            { title: '智能查询' },

          ]},
      ],
    }),
  }
</script>