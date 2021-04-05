# uni-app-pdf
   
博客地址(https://blog.csdn.net/M_Eve/article/details/106745067)

#### 介绍
在uni-app中使用pdf.js实现在手机上打开pdf

#### 安装教程

1.  git clone https://gitee.com/m_eve_admin/uni-app-pdf.git
2.  打开HBuilderX导入项目
3.  运行到手机查看效果图
![预览](https://gitee.com/m_eve_admin/pic/raw/master/img/view-pdf.png)

#### 使用说明

1.  将pdf.js下载的文件放到路径/hybrid/html下
2.  调用方法在index.vue中，具体查看注释即可

   
#### h5 跨域
另外如果h5想要跨域的话，可以配置你要访问的那个资源所在的服务，这里以 nginx 为例   

修改 nginx.conf 文件， 在location 下 添加 add_header 相关配置     
```
location / {
    root   html;
    index  index.html index.htm;

    add_header 'Access-Control-Allow-Origin' '*' always;
    add_header 'Access-Control-Allow-Credentials' 'true';
    add_header 'Access-Control-Allow-Methods' 'GET, POST, PATCH, DELETE, PUT, OPTIONS';
    add_header 'Access-Control-Allow-Headers' 'DNT,X-Mx-ReqToken,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type,  Access-Control-Expose-Headers, Token, Authorization';
}
```
