# pizza-app
### 项目描述 ######
是vue.js项目，是类似于一个点餐系统

### 功能 ######
 <p>用户登陆登出<p>
 <p>商品列表<p>
 <p>购物车列表<p>
 <p>商品管理（增删改）<p>
 <p>已购商品增，删<p>
 <p>网站信息<p>
 
 ### 技术栈 ######
 <p>Vue-cli<p>
 <p>Vue<p>
 <p>Vuex<p>
 <p>Vue-Router<p>
 <p>Axios<p>
 <p>Node<p>
 
  ### 数据 ######
 
 通过vuex管理整个应用状态的数据
 
 <p>删除商品</p>
  methods:{
      deleteData(item){
        fetch("https://wd2468178309upkmpi.wilddogio.com/menu/"+item.id+"/.json",{
          method:"DELETE",
          headers:{
            'Content-type':'application/json'
          }
        })
        .then(res => res.json())
        .then(data => {
          this.$store.commit('removeMenuItems',item)
        })
        .catch(err => console.log(err))
      }
    }
  }

 

![](https://github.com/dhyan123/p-app/blob/master/src/assets/1521797532(1).jpg)
> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
