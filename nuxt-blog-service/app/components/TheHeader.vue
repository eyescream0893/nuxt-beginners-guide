<template>
    <el-menu mode="horizontal" :router="true">
        <el-menu-item index="1" style="pointer-events:none">
            Nuxt Diary App
        </el-menu-item>
        <el-menu-item index="2" :router="{path: '/posts/'}">
            投稿一覧
        </el-menu-item>
        <el-menu-item index="3" style="floot: right" :route="{path: `/users/${user.id}`}" v-if="user">
            <span>{{user.id}}</span>
        </el-menu-item>
        <el-menu-item index="4" style="fotter: right;" :route="{path: '/'}" v-else>
            <span>ログイン</span>
        </el-menu-item>
        <el-menu-item index="5" style="fotter: right;" :route="{path: '/posts/new'}">
            新規投稿
        </el-menu-item>
    </el-menu>
</template>

<script>
import { mapGetters, mapActions } from 'vuex'
export default {
    computed: {
        ...mapGetters(['user'])
    }
}
</script>

