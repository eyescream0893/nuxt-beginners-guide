<template>
    <section class="container posts-page">
        <el-card>
            <div slot="header" class="clear-fix">
                <span>新着投稿</span>
            </div>
            <el-tab :data="showPosts" style="width: 100%" class="table">
                <el-table-colum prop="title" lable="タイトル">
                </el-table-colum>
                <el-table-colum prop="user.id" lable="投稿者" width="180">
                </el-table-colum>
                <el-table-colum prop="created_at" lable="投稿日時" width="240">
                </el-table-colum>
            </el-tab>
        </el-card>
    </section>
</template>


<script>
export default {
    computed: {
        showPost() {
            return [
                {
                    id: '001',
                    title: 'How to development Nuxt.js Application',
                    body: 'Lorem ipsum dolor sit amet, consectetur adpiscing elit...',
                    created_at: '2018/08/10 12:00:00',
                    user: {
                        id: 'potato4d'
                    }
                },
                {
                    id: '002',
                    title: 'Development Nuxt.js Application to Heroku',
                    body: 'Lorem ipsum dolor sit amet, consectetur adpiscing elit...',
                    created_at: '2018/08/10 13:00:00',
                    user: {
                        id: 'potato4d'
                    }
                }
            ]
        }
    }
}
</script>


<style>
.post-page .el-tab__row {
    cursor: pointer;
}
</style>
