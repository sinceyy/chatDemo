# chatDemo
静态页面部署方式
 server {
        listen       80;
        server_name  layui.com;
        location / {
            root   /home/data/code/;
            index  index.html index.htm;
        }
        location /layui/ {
            root   /home/data/code/;
            autoindex on;
        }

    }
    
自行更改host访问

lim启动方式
gunicorn --worker-class eventlet -w 1 app:app -b 0.0.0.0:5002

静态页面socket地址要和lim启动的ip地址保持一致，修改位置在layim/demo/index.html
