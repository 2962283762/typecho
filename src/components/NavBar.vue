<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container-fluid">
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo01"
                aria-controls="navbarTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarTogglerDemo01">
                <img src="data:image/png;base64,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"
                    alt="" class="logo col-1 offset-md-1">
                <ul class="navbar-nav mb-2 mb-lg-0 ul_css col-7">
                    <li class="nav-item ms-3 ">
                        <!-- <a class="nav-link active" aria-current="page" href="#">首页</a> -->
                        <router-link :to="{ name: 'home' }"
                            :class="route_name == 'home' ? 'nav-link selected_css' : 'nav-link select_css'">首页</router-link>
                    </li>
                    <li class="nav-item ms-3 select_css">
                        <!-- <a class="nav-link" href="#">关于</a> -->
                        <router-link :to="{ name: 'about' }"
                            :class="route_name == 'about' ? 'nav-link selected_css' : 'nav-link select_css'">关于</router-link>
                    </li>

                </ul>
                <div class="d-flex col-2" role="search">
                    <input class="search_input_css col-auto" type="search" placeholder="请输入关键字" aria-label="Search">
                    <button class="search_button_css col-auto" type="submit">搜索</button>
                </div>
            </div>
        </div>

    </nav>
    <div class="_class col-auto">
       <span style="color: #ccc;" class="offset-md-1">默认分类</span>
    </div>
</template>




<style scoped>
._class {
    width: 100%;
    box-shadow: 0 18px 18px rgb(230, 230, 230);

}

.select_css :hover {
    border-bottom: 3px solid rgb(78, 165, 255);
    color: rgb(78, 165, 255);
}

.selected_css {
    border-bottom: 3px solid rgb(78, 165, 255);
    color: rgb(78, 165, 255);
}

.logo {
    height: 7vh;

}

.search_input_css {
    border-radius: 30px 0 0 30px;
    height: 5vh;

    outline: none;
    background-color: rgb(235, 238, 245);
    border: 0;

}

.search_input_css:focus {
    background-color: white;
    border: 1px solid rgb(78, 165, 255);

}

.search_button_css {
    border-radius: 0 30px 30px 0;
    background-color: rgb(78, 165, 255);
    color: white;
    outline: none;
    height: 5vh;
    border-color: rgba(255, 255, 255, 0);
}

.ul_css {
    border-left: 1px solid rgb(235, 238, 245);
}

.container-fluid {
    border-bottom: 1px solid rgb(235, 238, 245);
}
</style>


<script>
import { useRoute } from 'vue-router'
import { computed } from 'vue'
export default {
    components: {

    },
    data() {
        return {

        }
    },
    setup() {
        const route = useRoute();
        let route_name = computed(() => route.name);
        return {
            route_name
        }
    }


}



</script>