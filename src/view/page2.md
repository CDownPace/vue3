# 生命周期组件
 ## setup() :开始创建组件之前，在beforeCreate 和 created 之前执行。创建的是data 和 method
## onBeforMount():组件挂载到节点上之前执行的函数
## onMounted():组件挂载到完成后执行的函数
## onUpdated():组件更新之前执行的函数
## onBeforeUpdated():组件更新之前执行的函数
## onUpdated():组件更新完成之后执行的函数
## onBeforeUnmount():组件卸载之前执行的函数
## onUnmounted():组件卸载完成之后执行的函数
## onActivated():被包含在<keep-alive>中的组件，会多出两个生命周期钩子函数。被激活时执行
## onDeactivated():比如从A组件，切换到B组件，A组件消失时执行
## onErrorCaptured():当捕获一个子孙组件的异常时激活钩子函数