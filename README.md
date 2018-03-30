#       717项目总结
##      1.搭建webpack
            判断开发环境和生产环境
##      2.页面
            首页
                搜索
            分类
                详情
            购物车
                编辑删除
            我的
                登录
                注册
                退出登录
                设置
            邮寄地址管理
                添加
                邮寄地址列表
            订单管理
##      3.路由搭建
            引用react-router { BrowserRouter , Route, NavLink } 三个组件搭建路由
##      4.传参
            封装组件，通过调用组件时在组建上props传参
##      5.组件封装
            首页，分类，购物车，我的，搜索，详情页，登录页，注册页，404页面，
            公共组件：
                商品展示页，轮播图
##      6.common组件封装
            弹出框
            轮播图
            商品模块
            数据懒加载
            默认图片展示
            购物车商品模块
            邮寄地址

##      7.技术选型

            搭建webpack,判断开发环境 （development） 和生产环境 （production），
            React, redux, react-router, react-redux, redux-sage
##      8.功能实现：
            首页：
                搜索：
                    封装搜索组件，把搜索框的value值存到本地存储，再渲染到最近搜索下，没有搜索内容显示"暂无搜索内容"
                轮播图组件：
                    swiper组件，
                商品展示组件：
                    封装组件，props传参，渲染数据，
                数据懒加载：
                    页面高度-(视口高度+滚动的高度)<50依赖这个公式去做数据懒加载
                默认图片展示:
                    react-lazyLoad: 参数（height，placeholder， debounce overflowonce））组件
                点击加入购物车：
                    组织事件冒泡，判断是否登录（getCookie是否有token这个字段），如果登录，把数据返回给后台，            后把返回的数据作为一个对象存到这个登录名下；如果没有登录跳转到登录页去登录
             分类：
                分为左右两部分，左边渲染食品类型，
                点击左边食品类型，传一个下标，右边根据下标去渲染食品
             购物车：
                引入redux，管理数据
                引入react-redux,拿到Provider顶层组件，包裹
                拿到数据，渲染页面
                点击加加减减，选中时在store中操作数据改变
             我的：
                判断有没有autherization这个字段，有的话再次判断是否登录，没有登录进入登录页面，已登录进入我的页面
                判断登录账号，渲染账号昵称
                登录页面
                注册页面
                设置：
                    添加收获地址
                    退出登录，操作token字段来设置退出登录
                    

        
