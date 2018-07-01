<template>
  <el-row class="tac">
    <el-col :span="4">
      <el-menu
        default-active="0-0"
        class="el-menu-vertical-demo"
        @open="handleOpen"
        @close="handleClose"
        unique-opened>
        <template v-for="(item, index) in menuList">
          <el-submenu :index="index+''" :key="index">
            <template slot="title">
              <span>{{item.name}}</span>
            </template>
            <el-menu-item-group v-for="(menuItem, menuIndex) in item.subName" :key="menuIndex" >
              <el-menu-item :index="index + '-' +menuIndex">{{menuItem}}</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </template>
      </el-menu>
    </el-col>
  </el-row>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      // isCollapse: true,
      menuList: [
        {name: '导航一', subName: ['Table', 'Form', '列表']},
        {name: '导航二', subName: ['页面四', '页面五']},
        {name: '导航三', subName: []},
        {name: '导航四', subName: ['Chart']},
      ],
    };
  },
  methods: {
    handleOpen (key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose (key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
