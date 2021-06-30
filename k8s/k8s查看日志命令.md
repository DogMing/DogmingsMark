# k8s 中常用的查日志的命令

日常开发过程中，有时候需要监控 k8s 容器中的日志。在 [k8s 命令文档](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands) 中学习到几个非常有用的命令。  

假如我有一个 deployment 名字是 app ，app 的 namespace 是 testns，并且有3个 rs ，pod 名字分别叫 app1,app2,app3 期中有每个 pod 有 c1,c2 两个 container


- kubectl logs app1 -n testns  
查看 pod app1 中第一个 container 的日志  

- kubectl logs -f app1 -n testns  
滚动查看 pod app1 中第一个container 的日志

- kubectl logs -f app1 -n testns --all-containers=true  
滚动查看 pod app1 中所有 container 的日志

- kubectl logs -lapp=app --all-containers=true  
查看label 匹配到 app=app 的 pod 的所有容器的日志

- kubectl logs -lapp=app -c c1  
查看所有匹配到 app=app 的 pod 中 c1 container 的日志，

- kubectl logs -lapp=app  
如果 pod 中只有一个容器，就可以省略掉指定容器的命令

- kubectl logs deployment/app --all-containers=true  
通过deployment 查看pod中容器的日志，前提是 pod 是通过 deployment 进行管理的