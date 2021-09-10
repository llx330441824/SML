# SML
微服务调用链路日志搜集(Simple Microservice Log)

https://blog.csdn.net/weixin_43776741/article/details/119701287

基于SMLFeignAnnotation和SMLLogAnnotation两个注解，结合美团CAT的基础功能，
以redis为存储介质，实现可配置化的分布式链路异常日志的搜集。

1.新增CatMethodAnnotation注解，完善CAT的接口调用计数功能
2.新增CatUrlAnnotation注解，完善CAT的URL跟踪
3.完善Cat的Mybatis拦截器，对输出的SQL类型可配置化
4.通过SMLFeignAnnotation和SMLLogAnnotation，实现链路调用唯一标识的传递，发生异常时将各个服务的异常堆栈信息进行搜集。
5.实现SMLAlertService接口，可自定义异常链路日志的通知实现方式
