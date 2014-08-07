schedule
=============

工作计划

## 增加命令行接口

让程序跑起来，如 `maria -p 22 --host 0.0.0.0 --host-key=./examples/host.key`

## 提供类似celery的命行令执行方式

比如 ``$celery -A tasks worker``  
-A 指定任务程序tasks.py.  

    app = Celery()  
    @app.run  
    def run()  
        pass  

然后可以在python中调用  

    from tasks import run  
    run()  

或者像gunicorn  

``gunicorn -b 0.0.0.0:2200 task:application``  

-b 绑定地址  
task 是任务程序  
application  是接口  

