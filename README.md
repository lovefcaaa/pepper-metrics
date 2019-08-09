# Pepper Metrics Project  
## Architecture  
### Concept
![](http://oss.zrbcool.top/picgo/pepper-metrics-concept.png-gh)
### Arch
![](http://oss.zrbcool.top/picgo/pepper-metrics-arch.png-gh)
> 各个组件说明
> - Profiler， 核心部分，用于启动定期调度任务，并通过ExtensionLoad加载所有的ScheduledRun扩展，按照指定周期发起调度。同时内部维护Stats的构造器Profiler.Builder
> - Scheduler， 虚拟概念，在Profiler作为一个定时任务存在
> - ExtensionLoader， 非常重要的组件，通过Java SPI机制加载插件，使项目的各个模块可以灵活插拔，也是项目架构的基石
> - ScheduledRun， 扩展点：pepper metrics core会定时调度，传递所有的Stats，实现插件可以使用Stats当中收集到的性能数据，目前已实现的为scheduled printer组件
> - Pepper Metrics X， 具体的集成，我们的目标是度量一切，目前计划实现的为：jedis，motan，dubbo，servlet，mybatis等最常用组件
## Getting started  
### Maven dependency  
### Next steps  
## Building  
## Contact  
* Bugs: [Issues](https://github.com/zrbcool/pepper-metrics/issues/new?template=dubbo-issue-report-template.md)
* Dingtalk chat group [Link](https://qr.dingtalk.com/action/joingroup?code=v1,k1,U4KKXEbTFBpuMbQMIQNij2IYszit+yktsAJh/9NjLFM=&_dt_no_comment=1&origin=11):  
![](http://oss.zrbcool.top/picgo/pepper-metrics-dingtalk-qrcode.png) 