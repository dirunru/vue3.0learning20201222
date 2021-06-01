# vue学习
#### vue创建方式有两种方法：
* cdn 引入方式：适合联系用
* vue脚手架@vue/cli 通过命令行去创建
#### vue computed计算属性
    computed有两种方法，默认是get方法，set方法可以做反向绑定，监听当前属性值，如果属性值发生改变，对属性反向修改。
#### vue声明周期中的渲染：
    beforeMount时还是通过 {{  变量名 }}的形式来展示的，此时还没有挂载到页面上，mounted之后才会进行挂载
    数据变化的时候会执行beforeUpdate和updated
    * 加载渲染过程
    父beforeCreate->父created->父beforeMount->子beforeCreate->子created->子beforeMount->子mounted->父mounted
    * 子组件更新过程
    父beforeUpdate->子beforeUpdate->子updated->父updated
    * 销毁过程
    父beforeDestroy->子beforeDestroy->子destroyed->父destroyed
