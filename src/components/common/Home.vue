<template>
    <div class="wrapper">
        <my-head></my-head>
        <my-sidebar></my-sidebar>
        <div class="content">
            <transition name="move" mode="out-in"><router-view></router-view></transition>
        </div>
    </div>
</template>

<script>
    import myHead from './Header.vue';
    import mySidebar from './Sidebar.vue';
    export default {
        components:{
            myHead, mySidebar
        }
    }
</script>
